<svelte:options tag={null} />

<!-- 2: add svelte options -->
<script>
  export let name = "toto";
  let count = 0;

  function incrementCount() {
    count += 1;
  }

  function resetCount() {
    count = 0;
  }
</script>

<main>
  <h1>I am {name}'s counter</h1>
  <p>{count} {count === 1 ? "time" : "times"}</p>
  <button on:click={incrementCount}> +1 </button>
  <button on:click={resetCount}> Reset </button>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    font-family: monospace;
  }

  button {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
    font-family: monospace;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
