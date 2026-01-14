<script lang="ts">
	import { inView } from '$lib/actions/animations';
</script>

<div class="section">
	<section id="about" class="about">
		<div class="about-text">
			<h1 use:inView class="section-text-title animate from-top">Who We Are</h1>
			<p use:inView class="section-text-content animate from-left">
				DeMo Technology, based in the greater Orlando area, bridges the gap between software and hardware. Coming from diverse backgrounds in software, simulation, themed entertainment, and electronics, our multidisciplinary team specializes
				in putting all of these together to create high-fidelity experiences supported by reliable backend systems.<br /><br />
				
				Our team has worked in the research space for years — collaborating with subject-matter experts to create both embedded systems and virtual educational experiences related to space exploration, satellite control, and aviation. Under Demo Technology, our team brings this research-oriented mindset
				to industry projects.
			</p>
		</div>
		<img
			use:inView
			class="about-img glow-sm animate from-right"
			src="/images/banners/colejosephbanner.jpg"
			alt="Profile"
		/>
	</section>
</div>

<style>
	h1 {
		text-align: left;
	}

	img {
		width: 100%;
		height: auto;
		border-color: var(--color-dark-primary);
		border-radius: 0.25rem;
		border-width: 0.3rem;
		border-style: solid;
		max-width: 34rem;
		max-height: 34rem;
		background-size: cover;
	}

	.section {
		max-width: 1280px;
	}

	.about {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(20rem, 1fr));
		justify-items: center;
		align-items: center;
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
		width: 100%;
		max-width: 52rem;
	}
</style>
