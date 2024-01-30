<script lang="ts">
	export let id: string
	// export let width = '1.2em'
</script>

<img
	alt="emoji"
	src="https://cdn.jsdelivr.net/gh/hfg-gmuend/openmoji/color/svg/{id.toUpperCase()}.svg"
/>

<!-- style="width: {width}; height: {width};" -->
<style>
	img {
		width: var(--font-size-fluid-3);
	}
</style>
