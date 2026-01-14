<script lang="ts">
	import { inView } from '$lib/actions/animations';
</script>

<div use:inView class="tagline animate">
	<div>
		<h1><slot /></h1>
	</div>
</div>

<style>
	.tagline {
		display: flex;
		justify-content: center;
		align-items: center;
		background-color: var(--color-dark-secondary);
		width: 100%;
	}

	.tagline div {
		padding: 6rem 2rem;
	}

	.tagline h1 {
		color: var(--color-light-primary);
		font-size: clamp(2rem, 2.5vw, 4rem);
		text-transform: uppercase;
		text-align: center;
		line-height: 1.25;
	}
</style>
