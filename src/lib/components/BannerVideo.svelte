<script lang="ts">
	export let height: string;
	export let src: string;
	export let autoplay = true;
	export let muted = true;
	export let loop = true;
</script>

<div class="banner" style="height: {height}">
	<video controls class="background" {autoplay} {muted} {loop} playsinline>
		<source src="{src}.webm" type="video/webm">

		<!-- MP4 source (fallback for browsers that don't support WebM) -->
		<source src="{src}.mp4" type="video/mp4">
	</video>
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
