<script lang="ts">
	export let height;
	export let img;
	export let position = 'center';
</script>

<div class="banner" style="height: {height}">
	<div class="parallax" style="min-height: {height}; background-image: url('{img}'); background-position: {position};"></div>
</div>

<style>
	.banner {
		position: relative;
		width: 100%;
		overflow: hidden;
	}

    .parallax {
		position: absolute;
        inset: 0;
		width: 100%;
		height: 100%;
		background-attachment: fixed;
		background-repeat: no-repeat;
		background-size: cover;
	}

	@media only screen and (max-width: 74rem) {
		.parallax {
			background-attachment: scroll;
		}
	}
</style>
