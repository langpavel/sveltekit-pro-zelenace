<script lang="ts" context="module">
	export const DEFAULT_SHEET_SIZE = '7x5cm';
	export const SHEET_SIZES = {
		[DEFAULT_SHEET_SIZE]: ['7cm', '5cm'],
		'10x6cm': ['10cm', '6cm']
	};
</script>

<script lang="ts">
	export let value = DEFAULT_SHEET_SIZE;
</script>

<select bind:value>
	{#each Object.entries(SHEET_SIZES) as [size, [width, height]]}
		<option value={size}>{width} × {height}</option>
	{/each}
</select>
