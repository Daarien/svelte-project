<script>
  import Counter from "./pages/Counter.svelte";
  import Music from "./pages/Music.svelte";
  import Buttons from "./pages/Buttons.svelte";

  const pages = ["Home", "Music", "Buttons"];

  let currentPage = pages[0];

  function setPage(event) {
    currentPage = event.target.id;
  }
</script>

<style lang="scss">
  :global(body) {
    margin: 0;
  }
  header {
    display: flex;
    align-items: center;
    padding: 0 10%;
    img {
      margin-right: 2rem;
    }
    h3 {
      color: darkmagenta;
    }
  }
  .layout {
    display: flex;
    padding: 1rem;
  }
  menu {
    flex-basis: 150px;
    margin: 0 2rem 0 0;

    li {
      margin-bottom: 0.5rem;
      list-style: none;
      padding: 5px 10px;
      color: darkmagenta;
      border: 2px solid darkorchid;
      background-color: white;
      cursor: pointer;
      transition: all 200ms;
      &.active {
        color: white;
        background-color: darkorchid;
      }
      &:hover {
        color: white;
        border-color: darkmagenta;
        background-color: darkmagenta;
      }
    }
  }
  main {
    flex-grow: 1;
  }
</style>

<!-- =================== styles ================= -->
<!-- =================== render ================== -->
<header>
  <img src="./assets/img/branding/svelte-logo.png" alt="Svelte logo" />
  <h3>Svelte Project</h3>
</header>

<div class="layout">
  <menu>
    <nav>
      {#each pages as page}
        <li id={page} on:click={setPage} class:active={currentPage === page}>
          {page}
        </li>
      {/each}
    </nav>
  </menu>

  <main>
    {#if currentPage === 'Home'}
      <p>Home page</p>
      <Counter />
    {/if}

    {#if currentPage === 'Music'}
      <Music />
    {/if}

    {#if currentPage === 'Buttons'}
      <Buttons />
    {/if}
  </main>
</div>
