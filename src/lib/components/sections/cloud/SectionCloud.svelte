<script lang="ts">
	import { inView } from '$lib/actions/animations';
	import CloudCard from './cards/CloudCard.svelte';
</script>

<div class="section">
	<section id="cloud" class="cloud">
		<div use:inView class="animate from-top">
			<h1 class="section-text-title">Cloud Services</h1>
			<p class="section-text-content">
				Our team can deploy any form of cloud service, such as software as a service (SaaS),
				multiplayer game servers, databases, and application programming interfaces (APIs).
			</p>
		</div>
		<div class="options">
			<CloudCard
				use={inView}
				classes="animate from-left"
				title="Backend Services"
				img="/images/cloud/cloud-icon.png"
				alt="cloud"
			>
				Our team is capable of deploying and maintaining cloud infrastructure. We have experience
				with dynamically scaling services to meet demand while minimizing cost.
			</CloudCard>
			<CloudCard
				use={inView}
				classes="animate from-bottom"
				title="Data Collection"
				img="/images/cloud/datacollection.png"
				alt="data collection"
			>
				The collection of large datasets are often required in science research, game servers, and
				many other industrial applications. We are experienced in the collection and processing of
				vast amounts of realtime data.
			</CloudCard>
			<CloudCard
				use={inView}
				classes="animate from-right"
				title="Game Servers"
				img="/images/cloud/gameserver.png"
				alt="gameserver"
			>
				Need dedicated game servers or ranked matchmaking systems? With our expertise in multiplayer
				game development, our team can build any system necessary.
			</CloudCard>
		</div>
	</section>
</div>

<style>
	h1 {
		text-align: center;
	}

	.cloud {
		display: grid;
		grid-template-columns: 1fr;
		gap: 4rem;
	}

	.options {
		width: 100%;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		align-items: center;
		gap: 1rem;
	}
</style>
