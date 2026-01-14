<script>
	export let id = '';
	export let use;
	export let classes;
	export let name;
	export let title;
	export let img;
	export let alt;
</script>

<div {id} use:use class={`profile ${classes}`}>
	<img src={img} {alt} />
	<h2>{name}</h2>
	<span>{title}</span>
</div>

<style>
	.profile {
		width: 50%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	img {
		width: 100%;
		border-radius: 100%;
		border-width: 0.4rem;
		border-style: solid;
		border-color: var(--color-dark-primary);
		box-shadow: 1px 1px 1px 1px black;
		max-width: 20rem;
		max-height: 20rem;
	}

	h2 {
		margin-top: 1rem;
		font-size: 2.25rem;
		color: var(--color-dark-primary);
		font-weight: 600;
	}

	span {
		margin-top: 1rem;
		font-size: 1.5rem;
		color: var(--color-dark-secondary);
		font-weight: 300;
	}

	@media (max-width: 74rem) {
		.profile {
			width: 100%;
			margin-bottom: 2rem;
		}

		.profile-title {
			width: 100%;
		}

		.profile-name {
			font-size: 2rem;
		}
	}
</style>
