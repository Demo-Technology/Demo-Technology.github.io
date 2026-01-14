<script lang="ts">
	import { inView } from '$lib/actions/animations';
	import Spacer from '$lib/components/Spacer.svelte';
	import ProfileIcon from './icons/ProfileIcon.svelte';
</script>

<div class="section">
	<section id="ourteam" class="ourteam">
		<h1 use:inView class="demoparent section-text-title animate from-top">
			Meet the &nbsp<span class="de">De</span>-<span class="mo">Mo</span>&nbsp behind DeMo Technology
		</h1>
		<Spacer width="80%" height="0.1rem" color="var(--color-dark-primary)" />
		<div class="profiles">
			<div id="josephprofile">
				<ProfileIcon
					use={inView}
					classes="animate from-bottom"
					img="/images/team/JosephDeMartiniProfile.png"
					alt="Joseph DeMartini"
					name="Joseph DeMartini"
					title="Co-Founder & Hardware Specialist"
				/>
			</div>
			<div id="coleprofile">
				<ProfileIcon
					use={inView}
					classes="animate from-bottom"
					img="/images/team/ColeMontroseProfile.jpg"
					alt="Cole Montrose"
					name="Cole Montrose"
					title="Co-Founder & Software Specialist"
					id="coleprofile"
				/>
			</div>
		</div>
	</section>
</div>

<style>
	h1 {
		text-align: center;
	}

	.ourteam {
		display:flex;
		flex-direction: column;
		align-items: center;
	}

	.profiles
	{
		margin-top: 4rem;
		display: grid;
		grid-template-columns: 1fr 1fr;
		justify-items: center;
		align-items: center;
		gap: 10rem;
	}

	.de
	{
		font-family:Futura Hv BT;
		text-transform: none;
	}

	.demoparent:has(.de:hover) ~ .profiles #josephprofile
	{
		transform:scale(1.1);
		transition:.25s;
	}

	.demoparent:has(.mo:hover) ~ .profiles #coleprofile
	{
		transform:scale(1.1);
		transition:.25s;
	}

	#josephprofile
	{
		transform:scale(1);
		transition:.25s;
	}

	#coleprofile
	{
		transform:scale(1);
		transition:.25s;
	}

	.mo
	{
		font-family:Futura Hv BT;
		text-transform: none;
	}

	@media (max-width: 74rem) {
		.profiles {
			grid-template-columns: 1fr;
			gap: 1rem;
		}
	}
</style>
