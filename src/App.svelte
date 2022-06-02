<script>
  import "./styles.css";
  import { onMount } from "svelte";
  import logo from "./assets/svelte.png";
  import Counter from "./lib/Counter.svelte";
  import { Button } from "@opentj/jui";
  import Switch from "heroicons/solid/switch-horizontal.svg";
  import { Icon } from "@steeze-ui/svelte-icon";
  import { Annotation } from "@steeze-ui/heroicons";
  // import {SwitchHorizontal} from '@steeze-ui/heroicons'

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
      mt-4
			inline-flex rounded-full border-2 border-solid
			border-gray-400 bg-green-400
			px-2 py-1 hover:bg-blue-400
			dark:border-red-500 dark:bg-slate-300
			dark:text-slate-600 dark:hover:bg-yellow-200"
    style=""
    on:click={() => toggleDarkMode()}
  >
    Toggle Light/Dark
    <Switch class="ml-3 mr-1 mt-[0.125rem] h-5 w-5" />
    <!--	  <Icon src={SwitchHorizontal} theme='solid' class='ml-3 mr-1 mt-[0.125rem] h-5 w-5'/>-->
  </Button>

  <div class="flex justify-around">
    <Icon src={Annotation} theme="solid" class="text-red-500" width={48} />
    <Icon src={Annotation} theme="default" class="text-red-500" width={48} />
  </div>

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
