<script lang="ts">
	import { inView } from '$lib/actions/animations';
</script>

<div class="section">
	<section id="xrtechnology" class="xr">
		<img
			use:inView
			class="xr-img glow-sm animate from-left"
			src="/images/xr/XRPhoto.jpg"
			alt="Profile"
		/>
		<div class="xr-text">
			<h1 use:inView class="section-text-title animate from-top">XR Technology</h1>
			<div use:inView class="animate from-right">
				<p class="section-text-content" style="margin-bottom: 0.5rem;">
					Extended Reality (XR) is an umbrella term for virtual, augmented, and mixed reality. Our
					team has collectively <strong>shipped 10+ educational VR titles</strong>, used by thousands
					of students. Our portfolio includes work with:
				</p>
				<br />
				<ul class="section-text-content sm">
					<li>- Projection mapping and custom depth tracking systems</li>
					<br />
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
		</div>
	</section>
</div>

<style>
	h1 {
		text-align: left;
	}

	img {
		border-color: var(--color-dark-primary);
		border-radius: 0.25rem;
		border-width: 0.3rem;
		border-style: solid;
		max-width: 25rem;
		max-height: 25rem;
		background-size: cover;
	}

	.section {
		max-width: 1280px;
	}

	.xr {
		display: grid;
		grid-template-columns: 30rem 1fr;
		justify-items: center;
		align-items: center;
		gap: 4rem;
	}

	@media (max-width: 74rem) {
		.xr {
			grid-template-columns: 1fr;
		}

		.xr-img {
			order: -1;
		}
	}

	.xr-text {
		max-width: 52rem;

		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;
	}
</style>
