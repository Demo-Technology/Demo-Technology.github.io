<script lang="ts">
	import { inView } from '$lib/actions/animations';
</script>

<div class="section">
	<div use:inView class="option animate from-left" >
		<div class="icon">
			<img src="/images/sensor.jpg" alt="hardware" />
		</div>
		<div class="title">
			Sensor Integration
		</div>
	</div>
	<div use:inView class="option animate from-above">
		<div class="icon">
			<img src="/images/hardware.jpg" alt="hardware" />
		</div>
		<div class="title">
			Hardware Prototyping
		</div>
	</div>
	<div use:inView class="option animate from-right">
		<div class="icon">
			<img src="/images/groundstation.jpg" alt="hardware" />
		</div>
		<div class="title">
			Ground Stations
		</div>
	</div>
</div>

<div class="section-text">
	<p use:inView class="section-text-content animate from-left">
		With our experience in building industry-level hardware, our team can prototype electronic systems to remotely collect data from sensors, prototype custom hardware devices and printed circuit boards, or even parallel process large amounts of data using FPGAs.
	</p>
	<p use:inView class="tagline animate from-right">
		The possibilities are endless — and we're here to create.
	</p>
</div>

<style>
	.tagline
	{
		display:flex;
		justify-content: center;
		align-items: center;

		margin-top: 2vh;
		font-size:50px;
	}

	.section-text
	{
		max-width:1280px;
		font-size: 22px;
	}

	.section {
		width: 100%;
		display:flex;
		justify-content: center;
		align-items: center;
	}

	.option
	{
		width: 23vw;
		height:26vh;

		margin-left: 1vw;
		margin-right: 1vw;
		margin-top: 1vw;

		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;

		box-shadow: 2px 2px 2px 2px black;
	}

	.icon
	{
		width:100%;
		height:75%;
		overflow: hidden;
	}

	.icon img
	{
		width:100%;
		background-size: cover;
	}

	.title
	{
		height:25%;
		width:100%;

		box-shadow: 2px 2px 2px 2px black;

		display:flex;
		justify-content: center;
		align-items: center;

		font-size: 20px;

		border-radius: 2px;
	}

	@media (max-width: 74rem) {
		.section
		{
			flex-direction: column;
		}
	}
</style>
