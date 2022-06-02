<script>
  import "./styles.css";
  import { onMount } from "svelte";
  import logo from "./assets/svelte.png";
  import Counter from "./lib/Counter.svelte";
  import { Button } from "@opentj/jui";

  const toggleDarkMode = function () {
    document.querySelector("html").classList.toggle("dark");
    // console.log(document.querySelector("html").classList);
  };
  onMount(() => {
    toggleDarkMode();
  });
</script>

<main>
  <img src={logo} alt="Svelte Logo" />
  <Counter />
  <div class="mt-4">Hello Tailwind CSS!</div>
  <Button
    class="
			mt-4 rounded-full border-2 border-solid
			border-gray-400 bg-green-400
			px-2 py-1 hover:bg-blue-400
			dark:border-red-500 dark:bg-slate-300
			dark:text-slate-600 dark:hover:bg-yellow-200"
    style=""
    on:click={() => toggleDarkMode()}
  >
    Toggle Light/Dark
  </Button>

  <!--	https://tailwindcss-forms.vercel.app/-->
  <!--	<input type="date" class="mt-1 block w-full">-->

  <!--	<div class="aspect-w-16 aspect-h-9">-->
  <!--		<iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>-->
  <!--	</div>-->
</main>

<style>
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
    height: 4rem;
    width: 4rem;
    align-content: center;
  }
</style>
