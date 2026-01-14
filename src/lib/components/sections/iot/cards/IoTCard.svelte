<script>
	export let id = '';
	export let use;
	export let classes;
	export let img;
	export let alt;
</script>

<div {id} use:use class={`${classes}`}>
	<div class="option">
		<div class="icon">
			<img src={img} {alt} />
		</div>
		<div class="title"><slot /></div>
	</div>
</div>

<style>
	.option {
		width: 100%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		background-color: var(--color-dark-primary);
		box-shadow: 5px 5px 10px rgba(0, 0, 0, 1);
		max-width: 24rem;
		height: 16rem;
		margin: 1rem;
		transition: transform 0.2s;
	}

	.option:hover {
		transform: scale(1.05);
	}

	.icon {
		width: 100%;
		height: 75%;
		overflow: hidden;
	}

	.icon img {
		width: 100%;
		background-size: cover;
	}

	.title {
		height: 25%;
		width: 100%;
		box-shadow: 2px 2px 2px 2px black;

		display: flex;
		justify-content: center;
		align-items: center;

		font-size: 20px;

		border-radius: 2px;
		color: var(--color-light-primary);
	}
</style>
