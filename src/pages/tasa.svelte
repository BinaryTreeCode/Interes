<script>
    let vf = 0;
    let I = 0;
  
    let i = 0;
    let t = 0;
  
    let c = 0;
    </script>
  
    <label>
      I <input type="number" bind:value={I} placeholder="I" /> /
     (c <input type="number" bind:value={c} placeholder="c" /> *
      t <input type="number" bind:value={t} placeholder="t" /> )
    </label>
    <p>i = {I / (c * t)}</p>
