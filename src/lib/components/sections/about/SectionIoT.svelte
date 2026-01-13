<script lang="ts">
	import { inView } from '$lib/actions/animations';
</script>

<div class="section">
	<section id="iot" class="iot">
		<div use:inView class="animate from-top">
			<h1 class="section-text-title">IoT & Electronics</h1>
			<p class="section-text-content">
				With our experience in building industry-level hardware, our team can prototype electronic
				systems to remotely collect data from sensors, prototype custom hardware devices and printed
				circuit boards, or even parallel process large amounts of data using FPGAs.
			</p>
		</div>
		<div class="cards">
			<div use:inView class="option animate from-left">
				<div class="icon">
					<img src="/images/sensor.jpg" alt="hardware" />
				</div>
				<div class="title">Sensor Integration</div>
			</div>
			<div use:inView class="option animate from-top">
				<div class="icon">
					<img src="/images/hardware.jpg" alt="hardware" />
				</div>
				<div class="title">Hardware Prototyping</div>
			</div>
			<div use:inView class="option animate from-right">
				<div class="icon">
					<img src="/images/groundstation.jpg" alt="hardware" />
				</div>
				<div class="title">Ground Stations</div>
			</div>
		</div>
		<div use:inView class="tagline animate">
			<h1>
				The possibilities are endless — and we're here to create.
			</h1>
		</div>
	</section>
</div>

<style>
	.section-text-title {
		text-align: center;
	}

	.iot {
		display: grid;
		grid-template-columns: 1fr;
		gap: 4rem;
	}

	.tagline {
		display: flex;
		justify-content: center;
		align-items: center;
		background-color: var(--color-text-primary);
		padding: 4rem 0;
		width: 100vw;
		margin: 0 calc(-50vw + 50%);
	}

	.tagline h1 {
		color: var(--color-background-primary);
		font-size: 3rem;
		text-align: center;
	}

	.cards {
		width: 100%;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		align-items: center;
	}

	.option {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		background-color: var(--color-text-primary);
		box-shadow: 5px 5px 10px rgba(0, 0, 0, 1);
		width: 24rem;
		height: 16rem;
		margin: 1rem;
	}

	.icon {
		width: 100%;
		height: 75%;
		overflow: hidden;
	}

	.icon img {
		width: 100%;
		background-size: cover;
	}

	.title {
		height: 25%;
		width: 100%;

		box-shadow: 2px 2px 2px 2px black;

		display: flex;
		justify-content: center;
		align-items: center;

		font-size: 20px;

		border-radius: 2px;
		color: var(--color-background-primary);
	}

	@media (max-width: 74rem) {
		.section {
			flex-direction: column;
		}
	}
</style>
