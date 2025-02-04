<script>
	import MediaQuery from "./MediaQuery.svelte";
</script>

<MediaQuery query="(min-width: 1281px)" >
	{#snippet children(matches)}
		{#if matches}
		<div class="root default">
			default
		</div>
		{/if}
	{/snippet}
</MediaQuery>

<MediaQuery query="(min-width: 481px) and (max-width: 1280px)" >
	{#snippet children(matches)}
		{#if matches}
		<div class="root tablet">
			tablet
		</div>
		{/if}
	{/snippet}
</MediaQuery>

<MediaQuery query="(max-width: 480px)" >
	{#snippet children(matches)}
		{#if matches}
		<div class="root mobile">
			mobile
		</div>
		{/if}
	{/snippet}
</MediaQuery>

<style>
	.root {
		position: fixed;
		left: 0;
		top: 0;
		right: 0;
		bottom: 0;
		padding: 1em;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	
	.default {
		background-color: white;
	}

	.tablet {
		background-color: antiquewhite;
	}

	.mobile {
		background-color: gold;
	}
</style>
