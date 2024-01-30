<script lang="ts">
	let dialog: HTMLDialogElement

	export function toggle() {
		dialog.open ? close() : open()
	}
	export function open() {
		dialog.showModal()
	}
	export function close() {
		dialog.close()
	}
</script>

<dialog bind:this={dialog}>
	<form method="dialog">
		<slot />
		<button>OK</button>
	</form>
</dialog>

<style>
	::backdrop {
		background: #0004;
		backdrop-filter: blur(2px);
		opacity: 0;
		animation: 0.3s fade-in forwards;
	}

	dialog[open] {
		padding: var(--size-7);
		color: var(--gray-2);
		border-radius: var(--radius-2);
		animation: var(--animation-slide-in-up) forwards;
	}

	dialog form {
		display: flex;
		flex-direction: column;
		gap: var(--size-4);
		justify-content: flex-end;
	}
</style>
