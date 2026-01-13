<script lang="ts">
	import { inView } from '$lib/actions/animations';
	import Spacer from '$lib/components/Spacer.svelte';
</script>

<div class="section-text">
	<p use:inView class="tagline animate from-right">
		Meet the &nbsp<span id="demo" style="font-family:Futura Hv BT;">DeMo</span>&nbsp behind DeMo Technologies
	</p>
	<br />
	<Spacer width="80%" height=".1vh" color="gray" />

	<div id="profiles">
		<div class="profile">
			<div class="profileimage">
				<img src="/images/ColeMontroseProfile.jpg" alt="profile">
			</div>
			<div class="profilename">
			Cole <b>Mo</b>ntrose
			</div>
			<div class="profiletitle">
			Co-Founder & Software Specialist
			</div>
		</div>
		<div class="profile">
			<div class="profileimage">
				<img src="/images/JosephDeMartiniProfile.png" alt="profile">
			</div>
			<div class="profilename">
			Joseph <b>De</b>Martini
			</div>
			<div class="profiletitle">
			Co-Founder & Hardware Specialist
			</div>
		</div>
	</div>
	
</div>

<style>
	.profilename
	{
		margin-top:1rem;
		font-size: 2.25rem;
	}

	.profiletitle
	{
		margin-top:1rem;
		font-size: 1.5rem;
	}

	#profiles
	{
		width: 80%;
		display: flex;
		justify-content: center;
		align-items: center;
		
		margin-top: 6vh;
	}

	.profile
	{
		width:50%;

		display:flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	.profileimage
	{
		width:60%;
	}

	.profileimage img
	{
		width:100%;
		border-radius:100%;
		border-width: 5px;
		border-style: ridge;
		border-color: black;
	}

	#demo
	{
		transform:scale(1);
		transition: .2s;
	}

	#demo:hover
	{
		transform:scale(1.2);
		transition: .2s;
	}

	.tagline
	{
		display:flex;
		justify-content: center;
		align-items: center;

		margin-top: 4vh;
		font-size:50px;
	}

	.section-text
	{
		width:100%;
		font-size: 22px;

		display:flex;
		flex-direction: column;
		align-items: center;
	}

	@media (max-width: 74rem) {
		
	}
</style>
