<script>
	import 'open-props/open-props.min.css'
	import 'open-props/normalize.min.css'
	import 'open-props/buttons.min.css'
	import 'open-props/masks/edges'
	import 'open-props/src/props.masks.edges.css'
	import 'open-props/masks.edges.min.css'

	import { dev } from '$app/environment'
	// import Header from '$lib/components/Header.svelte'
	import Footer from '$lib/components/Footer.svelte'
	// import Openmoji from '$lib/components/Openmoji.svelte'
</script>

<svelte:head>
	{#if !dev}
		<script
			async
			src="https://umami.haume.nz/script.js"
			data-website-id="67b5a50a-d032-4f08-b3b2-e8394a3321d8"></script>
	{/if}
</svelte:head>

<main>
	<!-- <Header /> -->
	<slot />
	<Footer />
</main>

<style>
	/* :global(*) {
		border: 1px solid salmon;
	} */
	:global(body) {
		display: flex;
		flex-direction: column;
		justify-content: start;

		min-height: 100vh;
	}
	/* :global(a, a:visited) {
		color: var(--jungle-10);
	}
	:global(a:hover) {
		text-decoration: none;
		color: var(--jungle-8);
	} */
	main {
		margin: var(--size-7);
	}
	@media (max-width: 640px) {
		main {
			margin: 0;
		}
	}
</style>
