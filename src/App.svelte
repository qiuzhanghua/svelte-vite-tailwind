<script>
	import './styles.css'
	import {onMount} from 'svelte'
 	import logo from './assets/svelte.png'
	import Counter from './lib/Counter.svelte'
	import {Button} from '@opentj/jui'
	
	const toggleDarkMode = function () {
		document.querySelector("html").classList.toggle("dark");
		console.log(document.querySelector("html").classList);
	}
	onMount(() => {
		toggleDarkMode()
	})

</script>

<main>
	<img src={logo} alt="Svelte Logo"/>
	<Counter/>
	<p></p>
	<div>Hello</div>
	<Button
			class="rounded-full bg-green-400 px-2 py-1 hover:bg-blue-400"
			style="border: solid"
			on:click={() => {
				toggleDarkMode();
		}}>Toggle Light/Dark
	</Button
	>

</main>

<style>
	:root {
		font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
		Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
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

	p {
		max-width: 14rem;
		margin: 1rem auto;
		line-height: 1.35;
	}

	@media (min-width: 480px) {
		p {
			max-width: none;
		}
	}
</style>
