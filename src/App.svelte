<script>
  import logo from "./assets/svelte.png";
  import Counter from "./lib/Counter.svelte";
</script>

<main class="pattern-grid-lg text-green-500 bg-black min-h-screen">
  <img src={logo} alt="Svelte Logo" />
  <div class="m-24 p-6 lg:p-12 bg-green-900 pattern-grid-sm">
	  <div class="text-white">
	  	<h1 class="text-[64px] lg:text-[200px]">Hell world!</h1>
	  	<Counter />
	  	<p>
	  			Visit <a href="https://svelte.dev">svelte.dev</a> to learn how to build Svelte
	  			apps.
	  	</p>
	  	<p>
	  			Check out <a href="https://github.com/sveltejs/kit#readme">SvelteKit</a> for
	  			the officially supported framework, also powered by Vite!
	  	</p>
	  </div>
  </div>
</main>

<style lang="postcss">
	@import '../node_modules/pattern.css/dist/pattern.min.css';
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }

  img {
    height: 16rem;
    width: 16rem;
  }

  h1 {
    text-transform: uppercase;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 14rem;
  }

  p {
    max-width: 14rem;
    margin: 1rem auto;
    line-height: 1.35;
  }

  @media (min-width: 480px) {
    h1 {
      max-width: none;
    }

    p {
      max-width: none;
    }
  }
</style>
