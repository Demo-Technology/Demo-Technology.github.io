<script lang="ts">
	import Hero from '$lib/components/Hero.svelte';
    import SectionAbout from '$lib/components/sections/about/SectionAbout.svelte';
	import Spacer from '$lib/components/Spacer.svelte';
	import SectionIoT from '$lib/components/sections/about/SectionIoT.svelte';
	import SectionCloud from '$lib/components/sections/about/SectionCloud.svelte';
	import XRBanner from '$lib/components/XRBanner.svelte';
	import SectionXR from '$lib/components/sections/about/SectionXR.svelte';
</script>

<Hero />

<main>
    <!-- ADD SECTIONS HERE -->
    <SectionAbout />
    <Spacer />
    <SectionIoT />
    <Spacer />
    <SectionCloud />
    <XRBanner />
    <SectionXR />
</main>
