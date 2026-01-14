<script lang="ts">
	import { inView } from '$lib/actions/animations';
	import IoTCard from './cards/IoTCard.svelte';
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
			<IoTCard use={inView} classes="animate from-left" img="/images/iot/sensor.jpg" alt="hardware">
				Sensor Integration
			</IoTCard>
			<IoTCard
				use={inView}
				classes="animate from-top"
				img="/images/iot/hardware.jpg"
				alt="hardware"
			>
				Hardware Prototyping
			</IoTCard>
			<IoTCard
				use={inView}
				classes="animate from-right"
				img="/images/iot/groundstation.jpg"
				alt="hardware"
			>
				Ground Stations
			</IoTCard>
		</div>
	</section>
</div>

<style>
	h1 {
		text-align: center;
	}

	.iot {
		display: grid;
		grid-template-columns: 1fr;
		gap: 4rem;
	}

	.cards {
		width: 100%;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		align-items: center;
		gap: 1rem;
	}
</style>
