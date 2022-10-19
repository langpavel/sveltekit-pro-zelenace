<script lang="ts" context="module">
    export type CSSSheetsDimensions = [string, string];
    export type SheetSize = '7x5cm' | '10x6cm';

	export const SHEET_SIZES: Record<SheetSize, CSSSheetsDimensions> = {
		'7x5cm': ['7cm', '5cm'],
		'10x6cm': ['10cm', '6cm']
	};
	export const DEFAULT_SHEET_SIZE = '7x5cm' as SheetSize;
</script>

<script lang="ts">
	export let value = DEFAULT_SHEET_SIZE;
</script>

<select bind:value>
	{#each Object.entries(SHEET_SIZES) as [size, [width, height]]}
		<option value={size}>{width} × {height}</option>
	{/each}
</select>
