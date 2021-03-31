
<script>
	import { onMount } from 'svelte';
	import { Paella } from 'paella-core';

	onMount(async () => {
		const paella = new Paella('player-container');

		paella.loadManifest()
			.then(() => console.log("Done"))
			.catch(err => console.log(err));
	});
</script>

<main>
	<h1>Hello from Svelte</h1>
	<div id="player-container"></div>
</main>

<style>
	div {
		width: 800px;
		height: 600px;
	}
</style>