<script lang="ts">
	export let height: string;
	export let src: string;
	export let autoplay = true;
	export let muted = true;
	export let loop = true;
</script>

<div class="banner" style="height: {height}">
	<video class="background" {src} {autoplay} {muted} {loop} playsinline></video>
</div>

<style>
	.banner {
		position: relative;
		width: 100%;
		overflow: hidden;
	}

	.background {
		position: absolute;
		inset: 0;
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: center;
		pointer-events: none;
	}
</style>
