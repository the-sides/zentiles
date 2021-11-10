<script>
  import { onDestroy, onMount } from "svelte";
  import logo from "./assets/svelte.png";
  import Board from "./lib/Board.svelte";
  onMount(() => {
    console.log("hi");
  });
  onDestroy(() => {
    console.log("bye");
  });
</script>

<main class="pattern-grid-xl text-green-500 bg-black min-h-screen">
  <div class="flex">
    <img class="h-32 w-32 hidden md:block" src={logo} alt="Svelte Logo" />
    <div class="mx-auto md:mx-4 p-6 bg-green-900 pattern-grid-sm">
      <h1 class="text-[64px] font-light text-white">Zentiles</h1>
    </div>
  </div>
  <div class="" />
  <div class="m-6 md:m-24 p-6 lg:p-12 bg-green-900 pattern-grid-sm">
    <div class="text-white">
      <Board />
    </div>
  </div>
</main>

<style lang="postcss">
  @import "../node_modules/pattern.css/dist/pattern.min.css";
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  }

  main {
    text-align: center;
    padding: 2em;
    margin: 0 auto;
  }
</style>
