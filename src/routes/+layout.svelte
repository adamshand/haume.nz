<script>
	import 'open-props/open-props.min.css'
	import 'open-props/normalize.min.css'
	import 'open-props/buttons.min.css'
	import 'open-props/masks/edges'
	import 'open-props/src/props.masks.edges.css'
	import 'open-props/masks.edges.min.css'

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

<main>
	<header>
		<!-- kite: 1FA81, earth:  1F30F -->
		<h1>Welcome</h1>
		<Openmoji id="1F30F" />
		<h1>Haume</h1>
	</header>

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
	main {
		margin-inline: var(--size-7);
	}
	:global(a) {
		color: var(--jungle-10);
	}
	:global(a:hover) {
		text-decoration: none;
		color: var(--jungle-8);
	}
	@media (max-width: 640px) {
		main {
			margin-inline: 0;
		}
	}
</style>
