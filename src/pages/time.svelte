<script>
    let vf = 0;
    let I = 0;
  
    let i = 0;
    let t = 0;
  
    let c = 0;
</script>
  
    <label>
      Ln( vf <input type="number" bind:value={vf} placeholder="vf" /> /
      c <input type="number" bind:value={c} placeholder="c" /> ) /
     Ln( 1 + i <input type="number" bind:value={i} placeholder="i" /> )
    </label>
    <p>t = {Math.log10(vf / c) / Math.log10(1 + i)}</p>
