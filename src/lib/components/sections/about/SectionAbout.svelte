<script lang="ts">
	import { inView } from '$lib/actions/animations';
</script>

<div class="section">
	<section id="about" class="about">
		<div class="about-text">
			<h1 use:inView class="section-text-title animate from-top">Who We Are</h1>
			<p use:inView class="section-text-content animate from-left">
				We are Demo Technology, a blah blah blah blah blah blah blah blah blah blah blah blah blah
				blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah blah
				blah blah blah blah blah blah blah blah blah blah blah blah blah company.
			</p>
		</div>
		<img
			use:inView
			class="about-img glow-sm animate from-right"
			src="/images/about/profile.jpg"
			alt="Profile"
		/>
	</section>
</div>

<style>
	h1 {
		text-align: left;
	}

	img {
		border-color: var(--color-background-alternate);
		border-radius: 2048px;
		border-width: 0.3rem;
		border-style: solid;
		max-width: 20rem;
		max-height: 20rem;
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
	}
</style>
