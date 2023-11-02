<script>
	import { onMount } from 'svelte';
	import '@esri/calcite-components/dist/calcite/calcite.css';

	onMount(async () => {
		console.log('mounted');
		const { setAssetPath } = await import('@esri/calcite-components/dist/components');
		setAssetPath('https://js.arcgis.com/calcite-components/1.10.0/assets');
		await import('@esri/calcite-components/dist/components/calcite-button');
	});
</script>

<calcite-button on:click={() => console.log('calcite button click')}>My Button</calcite-button>

<style>
</style>
