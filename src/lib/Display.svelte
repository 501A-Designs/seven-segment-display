<script lang="ts">
	import { numBin } from "../bin";
	import EmptySegment from "./EmptySegment.svelte";
	import FilledSegment from "./FilledSegment.svelte";
	export let num: any = 0;
	let bin: any = numBin[num][num];
	let indivBin: any = bin
		.toString()
		.split("")
		.map((iNum) => parseInt(iNum, 10));
	console.log("‎‍💻 Binary for " + num + " : " + bin);
	// console.log("Array form : " + indivBin);
	let a: number = indivBin[0];
	let b: number = indivBin[1];
	let c: number = indivBin[2];
	let d: number = indivBin[3];
	let e: number = indivBin[4];
	let f: number = indivBin[5];
	let g: number = indivBin[6];
</script>

<div class="display">
	<!-- A -->
	<EmptySegment />
	{#if a === 1}
		<FilledSegment />
	{:else}
		<EmptySegment />
	{/if}
	<EmptySegment />

	<!-- F -->
	{#if f === 1}
		<FilledSegment />
	{:else}
		<EmptySegment />
	{/if}
	<div class="emptyCenter" />

	<!-- B -->
	{#if b === 1}
		<FilledSegment />
	{:else}
		<EmptySegment />
	{/if}
	<EmptySegment />

	<!-- G -->
	{#if g === 1}
		<FilledSegment />
	{:else}
		<EmptySegment />
	{/if}
	<EmptySegment />

	<!-- E -->
	{#if e === 1}
		<FilledSegment />
	{:else}
		<EmptySegment />
	{/if}
	<div class="emptyCenter" />

	<!-- C -->
	{#if c === 1}
		<FilledSegment />
	{:else}
		<EmptySegment />
	{/if}
	<EmptySegment />

	<!-- D -->
	{#if d === 1}
		<FilledSegment />
	{:else}
		<EmptySegment />
	{/if}
	<EmptySegment />
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
</style>
