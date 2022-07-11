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
    Tienes el valor final (vf)
  </label>
  
  {#if yes}
    <label>
      vf <input type="number" bind:value={vf} placeholder="vf" /> -
      c <input type="number" bind:value={c} placeholder="c" /> 
    </label>
    <p>I = {vf - c}</p>
  {:else}
    <label>
      c<input type="number" bind:value={c} placeholder="c" /> *
      i<input type="number" bind:value={i} placeholder="i" /> *
      t<input type="number" bind:value={t} placeholder="t" />
    </label>
    <p>I = {c * i * t}</p>
  {/if}