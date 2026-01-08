<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';

	import '$lib/styles/reset.css';
	import '$lib/styles/global.css';
	import '$lib/styles/animations.css';
	import Nav from '$lib/components/Nav.svelte';
</script>

<svelte:head>
	<title>Demo Technology</title>
	<link rel="icon" href={favicon} />
</svelte:head>

<Nav />
<slot />
