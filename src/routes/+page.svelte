<script lang="ts">
	import Hero from '$lib/components/Hero.svelte';
    import SectionAbout from '$lib/components/sections/about/SectionAbout.svelte';
	import Spacer from '$lib/components/Spacer.svelte';
	import SectionIoT from '$lib/components/sections/about/SectionIoT.svelte';
	import SectionCloud from '$lib/components/sections/about/SectionCloud.svelte';
	import XRBanner from '$lib/components/XRBanner.svelte';
	import SectionXR from '$lib/components/sections/about/SectionXR.svelte';
	import SectionTeam from '$lib/components/sections/about/SectionTeam.svelte';
</script>

<Hero />

<main>
    <!-- ADD SECTIONS HERE -->
    <SectionAbout />
    <Spacer width="80%" color="var(--color-text-primary)" />
    <SectionIoT />
    <Spacer width="80%" color="var(--color-text-primary)" />
    <SectionCloud />
    <XRBanner />
    <SectionXR />
    <SectionTeam />
</main>
