<script lang="ts">
	import HorizontalDisplay from "./HorizontalDisplay.svelte";
	import VerticalDisplay from "./VerticalDisplay.svelte";
	export let num: any = 0;
</script>

<div class="display">
	<div class="emptySegment" />
	{#if num === 1}
		<div class="emptySegment" />
	{:else if num === 4}
		<div class="emptySegment" />
	{:else}
		<HorizontalDisplay />
	{/if}

	<div class="emptySegment" />
	{#if num === 1}
		<div class="emptySegment" />
	{:else if num === 2}
		<div class="emptySegment" />
	{:else if num === 3}
		<div class="emptySegment" />
	{:else if num === 7}
		<div class="emptySegment" />
	{:else}
		<VerticalDisplay />
	{/if}
	<div class="emptyCenter" />
	{#if num === 5}
		<div class="emptySegment" />
	{:else if num === 6}
		<div class="emptySegment" />
	{:else}
		<VerticalDisplay />
	{/if}
	<div class="emptySegment" />
	{#if num === 0}
		<div class="emptySegment" />
	{:else if num === 1}
		<div class="emptySegment" />
	{:else if num === 7}
		<div class="emptySegment" />
	{:else}
		<HorizontalDisplay />
	{/if}
	<div class="emptySegment" />
	{#if num === 1}
		<div class="emptySegment" />
	{:else if num === 3}
		<div class="emptySegment" />
	{:else if num === 4}
		<div class="emptySegment" />
	{:else if num === 5}
		<div class="emptySegment" />
	{:else if num === 7}
		<div class="emptySegment" />
	{:else if num === 9}
		<div class="emptySegment" />
	{:else}
		<VerticalDisplay />
	{/if}
	<div class="emptyCenter" />
	{#if num === 2}
		<div class="emptySegment" />
	{:else}
		<VerticalDisplay />
	{/if}

	<div class="emptySegment" />
	{#if num === 1}
		<div class="emptySegment" />
	{:else if num === 4}
		<div class="emptySegment" />
	{:else if num === 7}
		<div class="emptySegment" />
	{:else}
		<HorizontalDisplay />
	{/if}
	<div class="emptySegment" />
</div>

<style>
	.display {
		width: 65px;
		display: grid;
		grid-template-columns: 1fr 4fr 1fr;
		gap: 2px;
		margin-right: 5px;
		border-radius: 2px;
	}
	.emptyCenter {
		background-color: black;
		height: 40px;
		border-radius: 2px;
	}
	.emptySegment {
		background-color: black;
		min-width: 10px;
		min-height: 10px;
		border-radius: 2px;
	}
</style>
