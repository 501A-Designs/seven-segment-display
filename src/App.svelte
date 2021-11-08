<script lang="ts">
	import Display from "./lib/Display.svelte";
	export let number: any = 0;
	let numArray = [];
	const numArrayFunction = () => {
		numArray = number
			.toString()
			.split("")
			.map((iNum) => parseInt(iNum, 10));
		console.log(numArray);
	};
</script>

<main>
	<div>
		<h1>seven-segment-display</h1>
		<h2><a href="https://501a.netlify.app">made with svelte by 501A</a></h2>
		<p>
			currently only supports integers. If you open the console you can see the
			full list or arrays being rendered.
		</p>
		<input type="number" bind:value={number} on:input={numArrayFunction} />
	</div>
	<hr />
	<h3>>{numArray}</h3>
	<div class="flex">
		{#each numArray as i}
			<Display num={i} />
		{/each}
	</div>
</main>

<style>
	/* main {
		display: grid;
		grid-template-columns: 1fr 1fr;
	}
	main div {
		width: 300px;
	} */

	h1,
	h2 {
		margin: 0;
		padding: 0;
	}
	.flex {
		display: flex;
		gap: 5px;
	}
</style>
