<script>
	import 'open-props/open-props.min.css'
	import 'open-props/normalize.min.css'
	import 'open-props/buttons.min.css'

	import { dev } from '$app/environment'
	import Footer from '$lib/components/Footer.svelte'
	import Openmoji from '$lib/components/Openmoji.svelte'
</script>

<svelte:head>
	{#if !dev}
		<script
			async
			src="https://umami.haume.nz/script.js"
			data-website-id="67b5a50a-d032-4f08-b3b2-e8394a3321d8"
		></script>
	{/if}
</svelte:head>

<header>
	<!-- kite: 1FA81, earth:  1F30F -->
	<h1>Welcome</h1>
	<Openmoji id="1F30F" />
	<h1>Haume</h1>
</header>

<main>
	<slot />
</main>

<Footer />

<style>
	:global(*) {
		/* border: 1px solid salmon; */
	}
	:global(body) {
		display: flex;
		flex-direction: column;
		justify-content: start;

		min-height: 100vh;
	}
	header {
		display: flex;
		justify-content: center;
		align-items: center;
		gap: var(--size-3);
	}
	h1 {
		margin-block: var(--size-3);
		color: var(--text-2);
		font-size: var(--font-size-fluid-2);
	}
</style>
