<script lang="ts">
	export let id: string
	export let size: 's' | 'm' | 'l' = 'm'
	const src =
		'https://cdn.jsdelivr.net/gh/hfg-gmuend/openmoji/color/svg/' + id.toUpperCase() + '.svg'
</script>

<img alt="Openmoji icon" class={size} {src} />

<style>
	.s {
		width: var(--font-size-fluid-1);
	}
	.m {
		width: var(--font-size-fluid-2);
	}
	.l {
		width: var(--font-size-fluid-3);
	}
</style>
