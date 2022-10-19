<script lang="ts">
	import SheetSizeSelector, { DEFAULT_SHEET_SIZE } from '$lib/sheet-size/SheetSizeSelector.svelte';

	export let sheet = {
		title: '',
		size: DEFAULT_SHEET_SIZE,
	};
</script>

<form>
	<label>
		Velikost:
		<SheetSizeSelector bind:value={sheet.size} />
	</label>
	<label>Nadpis<input bind:value={sheet.title} /> </label>
</form>

<style>
	label {
		display: block;
	}
</style>
