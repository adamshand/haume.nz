<script lang="ts">
	import Openmoji from '$lib/components/Openmoji.svelte'
	import { shuffle } from '$lib/utils'

	// export let width = '2.5rem'

	const icons = [
		{ id: 'E046', link: 'https://www.linkedin.com/in/adamshand/' },
		{ id: '2709', link: 'mailto:kiaora@haume.nz' },
		{ id: 'E045', link: 'https://github.com/adamshand/' },
		{ id: '260E', link: 'tel:+64 21 499 772' },
    ]

	shuffle(icons)
</script>

<section>
	{#each icons as icon}
		{#if icon.link}
			<a href={icon.link} rel="me,noopener" target="_blank">
				<Openmoji id={icon.id} />
			</a>
		{:else}
    <a href={icon.link} rel="me,noopener" target="_blank">
      <!-- <Openmoji id={icon.id} {width} /> -->
      <Openmoji id={icon.id} />
    </a>  
		{/if}
	{/each}
</section>

<style>
	section {
		display: flex;
    justify-content: center;
    width: 100%;
    gap: var(--size-2);
	}
	a,
	a:hover {
		text-decoration: none;
	}
	a:hover {
		rotate: 5deg;
		transform: scale(1.1);
	}
</style>
