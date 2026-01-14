<script lang="ts">
	import { inView } from '$lib/actions/animations';
</script>

<div class="section">
	<section id="cloud" class="cloud">
		<div use:inView class="animate from-top">
			<h1 class="section-text-title">Cloud Services</h1>
			<p class="section-text-content">Our team</p>
		</div>
		<div use:inView class="option animate from-left">
			<div class="icon">
				<img src="/images/cloud-icon.png" alt="cloud" />
			</div>
			<div class="info">
				<div class="title">Backend Services</div>
				<div class="desc">AWS, Azure, you name it.</div>
			</div>
		</div>
		<div use:inView class="option animate from-left">
			<div class="icon">
				<img src="/images/datacollection.png" alt="data" />
			</div>
			<div class="info">
				<div class="title">Data Collection</div>
				<div class="desc">
					The collection of large datasets are often required in science research, game servers, and
					many other industrial applications. We are experienced in the collection and processing of
					vast amounts of realtime data.
				</div>
			</div>
		</div>
		<div use:inView class="option animate from-above">
			<div class="icon">
				<img src="/images/gameserver.png" alt="gameserver" />
			</div>
			<div class="info">
				<div class="title">Game Servers</div>
				<div class="desc">
					Need dedicated game servers or ranked matchmaking systems? With our expertise in
					multiplayer game development, our team can build any system necessary.
				</div>
			</div>
		</div>
	</section>
</div>

<div class="section-text">
	<p use:inView class="section-text-content animate from-left">
		<!-- With our experience in building industry-level hardware, our team can prototype electronic systems to remotely collect data from sensors, prototype custom hardware devices and printed circuit boards, or even parallel process large amounts of data using FPGAs. -->
	</p>
	<p use:inView class="tagline animate from-right">
		<!-- The possibilities are endless — and we're here to create. -->
	</p>
</div>

<style>
	h1 {
		text-align: center;
	}

	.title {
		width: 100%;
		height: 30%;
		font-size: 35px;

		display: flex;
		justify-content: flex-start;
		align-items: center;
	}

	.desc {
		width: 100%;
		height: 70%;
		font-size: 20px;
	}

	.tagline {
		display: flex;
		justify-content: center;
		align-items: center;

		margin-top: 2vh;
		font-size: 50px;
	}

	.section-text {
		max-width: 1280px;
		font-size: 22px;
	}

	.section {
		width: 100%;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		align-items: center;
	}

	.option {
		width: 26rem;
		height: 15rem;

		margin-left: 1vw;
		margin-right: 1vw;
		margin-top: 1vw;

		display: flex;
		justify-content: center;
		align-items: center;
	}

	.icon {
		width: 20%;
		height: 100%;
		overflow: hidden;

		padding-left: 10px;
	}

	.icon img {
		width: 100%;
		background-size: cover;
	}

	.info {
		height: 100%;
		width: 80%;

		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;

		font-size: 20px;

		border-radius: 2px;
		margin-left: 20px;
	}

	@media (max-width: 74rem) {
		.section {
			flex-direction: column;
		}
	}
</style>
