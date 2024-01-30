<script lang="ts">
	import Dialog from '$lib/components/Dialog.svelte'

	let dialog: Dialog
</script>

<h1>Dialog example</h1>

<button on:click={dialog.toggle}>Toggle</button>

<Dialog bind:this={dialog}>
	<p>This is a dialog!</p>
</Dialog>

<style>
	:global(body) {
		background: none;
		padding: 4rem;
		display: flex;
		flex-direction: column;
		align-items: flex-start;
		gap: 2rem;
	}

	h1 {
		color: var(--blue-4);
	}

	:global(button) {
		color: var(--blue-3);
	}
</style>
