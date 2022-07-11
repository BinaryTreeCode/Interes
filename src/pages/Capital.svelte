<script>
  let vf = 0;
  let I = 0;

  let i = 0;
  let t = 0;

  let c = 0;

  let yes = false;
</script>

<label>
  <input type="checkbox" bind:checked={yes} />
  Tienes el interes (I)
</label>

{#if yes}
  <label>
    I <input type="number" bind:value={I} placeholder="I" /> /
    (i <input type="number" bind:value={i} placeholder="i" /> *
    t <input type="number" bind:value={t} placeholder="t" />)
  </label>
  <p>C = {I / (i * t)}</p>
{:else}
  <label>
    <input type="number" bind:value={vf} placeholder="Vf" />
    <input type="number" bind:value={i} placeholder="i" />
    <input type="number" bind:value={t} placeholder="t" />
  </label>
  <p>C = {vf / (1 + i * t)}</p>
{/if}

<style>
  label {
    display: flex;
  }
  input,
  p {
    margin: 6px;
  }
</style>
