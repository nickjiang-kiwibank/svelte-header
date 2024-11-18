<svelte:options customElement="mdb-header" />

<script lang="ts">
  import Nav from "./nav.svelte";
</script>

<header>
  <div class="top">
    <h1>Kiwibank</h1>

    <slot name="my-text" class="slot1">My default text</slot>

    <input type="checkbox" id="toggler" checked />

    <aside class="aside-wrapper">
      <h1>this is side menu</h1>
    </aside>
  </div>
  <Nav />
</header>

<style>
  header {
    background-color: black;
    color: white;
  }
  header div {
    padding: 10px;
  }

  .top {
    display: flex;
    justify-content: space-between;
  }

  input:checked ~ aside {
    left: -250px;
  }
  aside {
    width: 250px;
    height: 100vh;
    background: blueviolet;
    position: fixed;
    top: 0;
    right: 0;
    height: 100vh;

    color: #fff;

    display: flex;
    flex-direction: column;
    justify-content: space-around;

    box-shadow: 3px 1px 5px 0px rgba(0, 0, 0, 0.75);
  }
</style>
