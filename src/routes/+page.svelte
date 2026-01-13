<script lang="ts">
	import Hero from '$lib/components/Hero.svelte';
	import Banner from '$lib/components/Banner.svelte';
    import SectionAbout from '$lib/components/sections/about/SectionAbout.svelte';
	import Nav from '$lib/components/Nav.svelte';
	import Spacer from '$lib/components/Spacer.svelte';
	import SectionIoT from '$lib/components/sections/about/SectionIoT.svelte';
</script>

<Hero />

<main>
    <!-- ADD SECTIONS HERE -->
    <SectionAbout />
    <Spacer />
    <SectionIoT />
    <Spacer />
</main>
