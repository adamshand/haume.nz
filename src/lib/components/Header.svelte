<script>
	import Openmoji from './Openmoji.svelte'
</script>

<!-- kite: 1FA81, earth:  1F30F -->
<header>
	<h1>Welcome</h1>
	<Openmoji id="1F30F" size="l" />
	<h1>Haume</h1>
</header>

<style>
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
