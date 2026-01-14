<script lang="ts">
	import { onMount } from 'svelte';

	let atTop = true;
	let open = false;

	onMount(() => {
		const onScroll = () => {
			atTop = window.scrollY < 100;
		};

		window.addEventListener('scroll', onScroll);
		onScroll();

		return () => {
			window.removeEventListener('scroll', onScroll);
		};
	});
</script>

<div class="nav-bar" class:transparent={atTop}>
	<a href="/" class="nav-bar-logo">
		<img class="nav-bar-logo-default" src={`/images/logos/${atTop ? 'w_logo' : 'b_logo'}.png`} alt="Company Logo" style="filter: drop-shadow(0 0 5px white);" />
        <img class="nav-bar-logo-glow" src={`/images/logos/${atTop ? 'w_logo_glow' : 'b_logo_glow'}.png`} alt="Company Logo" style="filter: drop-shadow(0 0 5px white);" />
	</a>
	<nav>
		<div class="nav-bar-links desktop">
            <a href="#about">About</a>
			<a href="#iot">IoT & Electronics</a>
			<a href="#cloud">Cloud Services</a>
			<a href="#xrtechnology">XR Technology</a>
			<a href="#ourteam">Our Team</a>
            <a href="#contact">Contact</a>
		</div>
		<button
			class="nav-bar-hamburger"
			class:open
			aria-label="Toggle navigation"
			aria-expanded={open}
			on:click={() => (open = !open)}
		>
			<span></span>
			<span></span>
			<span></span>
		</button>
		<div class="nav-bar-links mobile" class:open>
            <a href="#about" on:click={() => (open = false)}>About</a>
			<a href="#iot" on:click={() => (open = false)}>IoT & Electronics</a>
			<a href="#cloud" on:click={() => (open = false)}>Cloud Services</a>
			<a href="#xrtechnology" on:click={() => (open = false)}>XR Technology</a>
			<a href="#ourteam" on:click={() => (open = false)}>Our Team</a>
            <a href="#contact" on:click={() => (open = false)}>Contact</a>
		</div>
	</nav>
</div>

<style>
	.nav-bar {
		position: fixed;
		width: 100%;
		z-index: 10;
		background-color: var(--color-light-primary);
		border-bottom: 1px solid var(--color-dark-secondary);
		box-shadow: 0px 1px 5px rgba(0, 0, 0, 0.5);
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: space-between;
        transition:
			background-color 0.4s ease,
			border-bottom 0.2s ease,
            color 0.2s ease;
	}

    .nav-bar.transparent {
		background-color: rgb(3, 11, 37, 0);
		border-bottom: none;
		box-shadow: none;
	}

    .nav-bar.transparent .nav-bar-links a {
		color: var(--color-light-primary);
	}

	.nav-bar.transparent .nav-bar-links a:hover {
		color: var(--color-light-secondary);
	}

    .nav-bar.transparent .nav-bar-hamburger span {
		background: var(--color-light-primary);
	}

    .nav-bar.transparent .nav-bar-hamburger:hover span {
		background: var(--color-light-secondary);
	}

    .nav-bar.transparent .nav-bar-links.mobile {
		background-color: var(--color-dark-primary);
	}

	.nav-bar-logo {
		text-decoration: none;
		margin-left: 1.5rem;
		padding: 1rem 0;
		display: flex;
		flex-direction: row;
		align-items: center;
	}

	.nav-bar-logo img {
		max-width: 4rem;
		max-height: 4rem;
	}

    .nav-bar-logo .nav-bar-logo-default {
        display: block;
    }

    .nav-bar-logo .nav-bar-logo-glow {
        display: none;
    }

    .nav-bar-logo:hover .nav-bar-logo-default {
        display: none;
    }

    .nav-bar-logo:hover .nav-bar-logo-glow {
        display: block;
    }

	.nav-bar-links {
		display: flex;
		justify-content: flex-end;
		align-items: flex-end;
	}

	.nav-bar-links a {
		position: relative;
		color: var(--color-dark-primary);
		text-decoration: none;
		font-size: 1.5rem;
		font-weight: 100;
		transition: color 0.4s;
	}

	.nav-bar-links a:hover {
		color: var(--color-dark-secondary);
	}

	.nav-bar-links a::after {
		content: '';
		position: absolute;
		left: 0;
		bottom: -4px;
		width: 0;
		height: 2px;
		background: currentColor;
		transition: width 0.4s ease;
	}

	.nav-bar-links a:hover::after {
		width: 100%;
	}

	.nav-bar-links.desktop {
		display: flex;
		flex-direction: row;
		margin-right: 1.5rem;
		gap: 3rem;
	}

	.nav-bar-links.mobile {
		display: none;
		opacity: 0;
		position: absolute;
		right: 1rem;
		pointer-events: none;
		flex-direction: column;
		align-items: flex-end;
		background-color: var(--color-light-primary);
		border: 1px solid var(--color-dark-secondary);
		box-shadow: 0px 5px 10px rgba(0, 0, 0, 1);
		border-radius: 10px;
		gap: 1.5rem;
		margin-top: 2.5rem;
		padding: 1.5rem;
		transition: 
            opacity 0.2s ease,
            background-color 0.4s ease;
	}

	.nav-bar-links.mobile.open {
		opacity: 1;
		pointer-events: auto;
	}

	.nav-bar-hamburger {
		display: none;
		flex-direction: column;
		margin-right: 1.5rem;
		gap: 0.35rem;
		justify-content: center;
		cursor: pointer;
	}

	.nav-bar-hamburger span {
		width: 1.75rem;
		height: 0.25rem;
		border-radius: 1rem;
		background: var(--color-dark-primary);
		transition: background 0.4s;
	}

	.nav-bar-hamburger:hover span {
		background: var(--color-dark-secondary);
	}

	.nav-bar-hamburger.open span {
		background: var(--color-dark-secondary);
	}

	@media (max-width: 70rem) {
		.nav-bar-links.desktop {
			display: none;
		}

		.nav-bar-links.mobile {
			display: flex;
		}

		.nav-bar-hamburger {
			display: flex;
		}
	}
</style>