<script lang="ts">
	import Hero from '$lib/components/Hero.svelte';
	import SectionAbout from '$lib/components/sections/about/SectionAbout.svelte';
	import Spacer from '$lib/components/Spacer.svelte';
	import SectionIoT from '$lib/components/sections/iot/SectionIoT.svelte';
	import SectionCloud from '$lib/components/sections/cloud/SectionCloud.svelte';
	import XRBanner from '$lib/components/XRBanner.svelte';
	import SectionXR from '$lib/components/sections/xr/SectionXR.svelte';
	import SectionTeam from '$lib/components/sections/team/SectionTeam.svelte';
	import SectionContact from '$lib/components/sections/contact/SectionContact.svelte';
	import BannerImage from '$lib/components/BannerImage.svelte';
	import BannerText from '$lib/components/BannerText.svelte';
</script>

<Hero />

<main>
	<!-- ADD SECTIONS HERE -->
	<SectionAbout />
	<BannerImage height="35rem" img="/images/banners/computerhardwarebanner.jpg" position="center" />
	<SectionIoT />
    <BannerText>Building IoT solutions that connect the physical and digital worlds.</BannerText>
	<SectionCloud />
	<BannerImage height="30rem" img="/images/banners/gamejambanner.jpg" position="center" />
	<SectionXR />
	<SectionTeam />
	<SectionContact />
</main>

<style>
	.parallax {
		/* The image used */
		background-image: url('img_parallax.jpg');

		/* Set a specific height */
		min-height: 500px;

		/* Create the parallax scrolling effect */
		background-attachment: fixed;
		background-position: center;
		background-repeat: no-repeat;
		background-size: cover;
	}
</style>
