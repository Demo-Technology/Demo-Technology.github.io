<script lang="ts">
	import { inView } from '$lib/actions/animations';
	import Spacer from './Spacer.svelte';
</script>

<section class="background">
    <div class="el">
        <div class="text">
            <h1 use:inView class="animate from-top">The Possibilities are Endless and We're Here to Create</h1>
            <Spacer width="80%" color="var(--color-background-primary)" />
            <h2 use:inView class="animate from-bottom">DeMo Technology</h2>
        </div>
    </div>
</section>

<style>
    .text {
        position: relative;
		z-index: 1;
        display: flex;
        flex-direction: column;
        gap: 3rem;
        padding: 0 1rem;
    }

	.text h1 {
		text-align: center;
		position: relative;
		font-size: clamp(3rem, 12vw, 6rem);
		font-weight: 500;
		color: var(--color-background-primary);
		text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
	}

	.text h2 {
		text-align: center;
		position: relative;
		font-size: clamp(1.5rem, 4vw, 3rem);
		font-weight: 300;
		color: var(--color-background-primary);
		text-shadow: 2px 2px 2px rgba(0, 0, 0, 0.5);
	}

	* {
		box-sizing: border-box;
	}

	:root {
		--size: 20px;
	}

	.background {
		display: grid;
		place-items: center;
		min-height: 100vh;
        background-color: var(--color-text-primary);
	}

	.el {
		position: relative;
		display: grid;
		place-items: center;
		width: 100%;
		height: 100%;
	}

	.el::before {
		content: '';
		position: absolute;
		inset: 0;
		background: conic-gradient(
			from 180deg at 50% 70%,
			hsla(0, 0%, 98%, 1) 0deg,
			#eec32d 72deg,
			#ec4b4b 144deg,
			#709ab9 216deg,
			#4dffbf 288deg,
			hsla(0, 0%, 98%, 1) 1turn
		);

		mask:
			radial-gradient(circle at 50% 50%, white 2px, transparent 2.5px) 50% 50% / var(--size)
				var(--size),
			url('https://assets.codepen.io/605876/noise-mask.png') 256px 50% / 256px 256px;

		mask-composite: intersect;
		animation: flicker 20s linear infinite;
		z-index: 0;
	}

	@keyframes flicker {
		to {
			mask-position:
				50% 50%,
				0 50%;
		}
	}
</style>
