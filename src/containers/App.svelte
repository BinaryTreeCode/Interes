<script>
    import Capital from '../pages/Capital.svelte';
    import Interés from '../pages/Interés.svelte';
    import tasa from '../pages/tasa.svelte';
    import time from '../pages/time.svelte';
    import Vf from '../pages/Vf.svelte';

    let currentPage ;
  function changePage(newPage) {
    currentPage = newPage;
  }
  function changePageVf() {
    changePage(Vf)
  }
</script>

<div>
  <div class="nav">
    <button on:click={() => changePage(Capital)}>Capital</button>
    <button on:click={() => changePage(Interés)}>Interés</button>
    <button on:click={() => changePage(tasa)}>tasa</button>

    <button on:click={() => changePage(time)}>tiempo</button>
    <button on:click={() => changePage(Vf)}>valor final</button>
  </div>
  <div class="contend">
    <section>
        <p>El interés simple es el interés(benéfico) que se obtiene de una inversión, y mide los intereses producidos durante cada periodo de tiempo de la inversión. 
          Los intereses no se acumulan al capital, siempre se aplican sobre el mismo capital, son pagados periodo a periodo, por lo que el interés siempre es el mismo.
          En el juego de los intereses aplican varias variables como lo son: </p>
          <div class="grid">
            <div>C = capital invertido</div>
            <div>
              C = I / (i * t)
              <br> 
              C = Vf / 1+ (i * t)
            </div>
            
            <div>I = interés</div>
            <div>
              I = Vf – c
              <br>
              I = c * i * t
            </div>

            <div>i = tasa de interés</div>
            <div>
              I = c * i * t
            </div>

            <div>t = tiempo</div>
            <div>
              t = I / (c * i)
            </div>

            <div>Vf = valor final</div>
            <div>
              Vf = c + I
              <br>
              Vf = c (1+ i)^t
            </div>
          </div>
    </section>
    <svelte:component this={currentPage} />
  </div>
</div>

<style>
  :global(body) {
    background-color: #676778;
    color: white;
  }
  .nav {
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 1rem;
  }
  
  .contend {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        padding: 1rem;

        padding-top: 0;

        font-size: 20px;

        position: relative;
    }
    .nav button {
        background-color: #676778;
        color: white;
        border: none;
        padding: 1rem;
        border-radius: 5px;
        font-size: 20px;
    }

    .nav button:hover {
        background-color: #ffffff;
        color: black;
        border: none;
        padding: 0.5rem;
        border-radius: 5px;
        font-size: 20px;
    }

    .nav button:active {
        background-color: black;
        color: white;
        border: none;
        padding: 0.5rem;
        border-radius: 5px;
        font-size: 20px;
    }

    .grid {
        display: grid;
        grid-template-columns: repeat(5, 1fr);
        grid-template-rows: repeat(2, 1fr);

        grid-auto-flow: column;

        padding-bottom: 1.5rem;
    }
</style>
