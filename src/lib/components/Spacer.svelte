<script lang="ts">
	export let id = '';
    export let width = '60%';
    export let height = '0.001vh';
    export let color;
</script>

<div class="spacer">
    <div {id} style="width: {width}; height: {height}; box-shadow: 2px 2px 2px 2px {color}; background-color: {color}"></div>
</div>

<style>
    .spacer {
        display: flex;
        justify-content: center;
    }
</style>