<script>
    import Capital from '../pages/Capital.svelte';
	import Interés from '../pages/Interés.svelte';
    import tasa from '../pages/tasa.svelte';
    import time from '../pages/time.svelte';
    import Vf from '../pages/Vf.svelte';

  let currentPage = Home;

  function changePage(newPage) {
    currentPage = newPage;
  }
</script>

<div>
  <div class="nav">
    <button on:click={() => changePage(Capital)}>Capital</button>
    <button on:click={() => changePage(Interés)}>Interés</button>
    <button on:click={() => changePage(tasa)}>tasa</button>

    <button on:click={() => changePage(time)}>time</button>
    <button on:click={() => changePage(Vf)}>Vf</button>
  </div>
  <div>
    <svelte:component this={currentPage} />
  </div>
</div>

<style>
  :global(body) {
    background-color: #676778;
    color: white;
  }
</style>
