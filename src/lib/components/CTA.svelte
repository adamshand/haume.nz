<script>
	import Openmoji from '$lib/components/Openmoji.svelte'
</script>

<section>
	<!-- <h2>Get in touch?</h2> -->
	<a href="https://cal.com/adamshand/twenty">
		<button> <Openmoji id="1F4C5" size="m" /> Free Discovery Call</button>
	</a>
	<p style="text-align: center">
		Book a free 20 minute discovery call. No obligation or presssure. Just a friendly chat to see if
		I can help. Or do it the old fashioned way, and give me a call.
	</p>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		align-items: center;
		padding-block: var(--size-5);
	}
	p {
		margin-inline: var(--size-fluid-4);
		color: var(--text-2);
		font-style: italic;
	}
	button {
		margin-bottom: var(--size-3);
		background-color: var(--jungle-9);
		border: 1px solid var(--jungle-11);
		color: var(--surface-1);
		text-shadow: none;

		&:hover {
			background-color: var(--jungle-8);
		}
	}
</style>
