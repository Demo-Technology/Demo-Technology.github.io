<section>
    <div class="background">
        <div class="el"></div>
    </div>
</section>

<style>

    .hero {
		position: relative;
		height: 100vh;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		overflow: hidden;
	}

	.banner {
		height: 80vh;
		overflow: hidden;
	}

	.banner img {
		object-fit: cover;
		object-position: center;
		filter: blur(4px);
		width: 100%;
		height: 100%;
	}

    h1 {
		position: fixed;
		top: 50%;
		left: 50%;
		translate: -50% -50%;
		margin: 0;
		font-size: clamp(6rem, 8vw + 1rem, 14rem);
		font-family: 'Geist', sans-serif;
		font-weight: 140;
		color: hsl(0 0% 2%);
		mix-blend-mode: soft-light;
		/*   -webkit-text-stroke: 2px hsl(0 0% 100% / 0.95); */
		filter: drop-shadow(0 0 2px white);
		text-shadow: 2px 2px white;
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
		background: hsl(0 0% 6%);
	}

	.el {
		background: conic-gradient(
			from 180deg at 50% 70%,
			hsla(0, 0%, 98%, 1) 0deg,
			#eec32d 72.0000010728836deg,
			#ec4b4b 144.0000021457672deg,
			#709ab9 216.00000858306885deg,
			#4dffbf 288.0000042915344deg,
			hsla(0, 0%, 98%, 1) 1turn
		);
		width: 100%;
		height: 100%;
		mask:
			radial-gradient(circle at 50% 50%, white 2px, transparent 2.5px) 50% 50% / var(--size)
				var(--size),
			url('https://assets.codepen.io/605876/noise-mask.png') 256px 50% / 256px 256px;
		mask-composite: intersect;
		animation: flicker 20s infinite linear;
	}

	@keyframes flicker {
		to {
			mask-position:
				50% 50%,
				0 50%;
		}
	}
</style>
