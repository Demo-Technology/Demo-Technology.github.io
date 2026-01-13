<script lang="ts">
	import { inView } from '$lib/actions/animations';
	import Spacer from '$lib/components/Spacer.svelte';
</script>

<section id="xrtechnology" class="section">
	<section id="about" class="about">
		<div class="about-text">
			<h1 use:inView class="section-text-title animate from-top">XR Technology</h1>
			<p use:inView class="section-text-content animate from-left" style="padding-bottom:3vh;">
			Extended Reality (XR) is an umbrella term for virtual, augmented, and mixed reality. Our team has collectively <strong>shipped 10+ educational VR titles</strong>,
			used by thousands of students. Our portfolio includes:</p><br />
			<ul>
				<li>- SteamVR and OpenXR Frameworks</li>
				<br />
				<li>- Custom-built XR hardware</li>
				<br />
				<li>- Motion platform integration and custom safety systems</li>
				<br />
				<li>- Custom VR/AR applications for Valve Index, Varjo, Quest, Magic Leap headsets</li>
			<br />
			</ul>
		</div>
		<img
			use:inView
			class="about-img glow-sm animate from-right"
			src="/images/XRPhoto.jpg"
			alt="Profile"
		/>
	</section>
</section>

<style>
	h1 {
		text-align: left;
	}

	img {
		border-color: var(--color-background-alternate);
		border-radius: 0vw;
		border-width: 0.3rem;
		border-style: solid;
		max-width: 25rem;
		max-height: 25rem;

		background-size:cover;
	}

	.section {
		max-width: 1280px;
	}

	.about {
		display: grid;
		grid-template-columns: 1fr 30rem;
		justify-items: center;
		gap: 4rem;
	}

	@media (max-width: 74rem) {
		.about {
			grid-template-columns: 1fr;
		}

		.about-img {
			order: -1;
		}
	}

	.about-text {
		max-width: 52rem;

		display:flex;
		flex-direction: column;
		justify-content: center;
		align-items:flex-start;
	}
</style>
