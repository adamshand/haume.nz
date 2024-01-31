<script lant="ts">
	import CTA from '$lib/components/CTA.svelte'
	import Socials from '$lib/components/Socials.svelte'
</script>

<!-- src="https://pb.haume.nz/api/files/amu003xvt8ezymb/i9abatyw4ug5ag9/cables_Hrw92cz83c.jpg?token=" -->
<section>
	<img
		src="https://pb.haume.nz/api/files/amu003xvt8ezymb/i9abatyw4ug5ag9/audrey_4hIFaCF5f1.jpg?token="
		alt="square" />
	<article>
		<h2>Kia ora,</h2>

		<p>
			<b>I’m Adam, a freelancer on New Zealand’s Kāpiti Coast.</b>
		</p>
		<p>
			I mostly work with individuals and small businesses. I usually bill by the hour and am happy
			to take on small projects. My speciality is helping you determine how best to deploy
			technology to meet your personal or business needs (and then building whatever is required).
			I'm a believer in less-is-more when it comes to technology and want to help you make the most
			of what you already have. Some of my favourite tools include Debian Linux, macOS, Docker,
			JavaScript, and SvelteKit.
		</p>

		<p>
			I've been working in technology since the early 90s when I built one of New Zealand's first
			dialup ISPs. I spent the late 90s and early 2000s in the United States working for a variety
			of dot-com startups. In 2003 I moved back to Wellington to work with (and later manage) Weta
			Digital's infrastructure team where I got to work on a bunch of amazing projects including
			<em>The Lord of the Rings</em> and <em>Avatar</em>.
		</p>
		<p>
			I have long-standing interests and practices in regenerative agriculture, espresso, nonviolent
			communication, vipassanā meditation, ketogenic diets, and open source software.
		</p>
	</article>
</section>

<div>
	<CTA />
	<Socials />
</div>

<style>
	section {
		display: flex;
		justify-content: start;
		align-items: top;

		padding-inline: var(--size-5);
		padding-block: var(--size-8);
		background-color: var(--surface-2);
		color: var(--text-2);
		border-radius: var(--radius-conditional-3);
		mask: var(--mask-edge-zig-zag-bottom);
		-webkit-mask: var(--mask-edge-zig-zag-bottom);
	}
	img {
		height: var(--size-fluid-9);
		border-radius: var(--radius-blob-4);
		box-shadow: var(--shadow-6);
	}
	article {
		flex: 1;
		margin-left: var(--size-fluid-3);
	}
	h2 {
		margin-bottom: var(--size-fluid-1);
		color: var(--jungle-9);
		font-size: var(--font-size-fluid-2);
	}
	p {
		margin-bottom: var(--size-3);
		color: var(--text-2);
	}
	div {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding-block: var(--size-5);
	}

	@media (max-width: 640px) {
		section {
			flex-direction: column;
			align-items: center;
		}

		img {
			width: 100%;
			height: auto;
			margin-bottom: var(--size-fluid-2);
		}
	}
</style>
