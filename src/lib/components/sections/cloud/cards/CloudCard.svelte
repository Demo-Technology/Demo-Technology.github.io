<script>
	export let id = '';
	export let use;
	export let classes;
	export let title;
	export let img;
	export let alt;
</script>

<div {id} use:use class={`option ${classes}`}>
	<div class="icon">
		<img src={img} {alt} />
	</div>
	<div class="info">
		<div class="title">{title}</div>
		<p class="desc">
			<slot />
		</p>
	</div>
</div>

<style>
	.option {
		width: 100%;
		max-width: 24rem;
		height: 20rem;

		margin-left: 1vw;
		margin-right: 1vw;
		margin-top: 1vw;

		display: flex;
		justify-content: center;
		align-items: center;
	}

	.icon {
		width: 20%;
		height: 100%;
		overflow: hidden;

		padding-left: 10px;
	}

	.icon img {
		width: 100%;
		background-size: cover;
	}

	.info {
		height: 100%;
		width: 80%;

		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;

		font-size: 20px;

		border-radius: 2px;
		margin-left: 20px;
	}

	.title {
		width: 100%;
		height: 30%;
		font-size: 2rem;
		color: var(--color-dark-primary);
		font-weight: 350;
		line-height: 1.15;
		display: flex;
		justify-content: flex-start;
		align-items: center;
	}

	.desc {
		width: 100%;
		height: 70%;
		font-size: 1.25rem;
		color: var(--color-dark-primary);
		font-weight: 350;
		line-height: 1.15;
	}
</style>
