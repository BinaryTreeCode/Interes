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
    Tienes el interés compuesto (I)
  </label>
  
  {#if yes}
    <label>
       c <input type="number" bind:value={c} placeholder="c" /> 
       I <input type="number" bind:value={I} placeholder="I" /> +
    </label>
    <p>I = {c + I}</p>
  {:else}
    <label>
      c <input type="number" bind:value={c} placeholder="c" /> ( 1 +
      i <input type="number" bind:value={i} placeholder="i" /> ) ^
      t <input type="number" bind:value={t} placeholder="t" />
    </label>
    <p>I = {c ((1 * i)**t)}</p>
  {/if}