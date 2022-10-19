<script lang="ts">
	import { DEFAULT_SHEET_SIZE } from "$lib/sheet-size/SheetSizeSelector.svelte";
	import Sheet from "$lib/sheet/Sheet.svelte";

    let sheet = {
        size: DEFAULT_SHEET_SIZE,
        title: 'TETS'
    }
</script>

<main>
    <h1>Tisk stitku</h1>
    <Sheet bind:sheet />

    <Sheet bind:sheet />

    <pre>{JSON.stringify(sheet, null, 2)}</pre>

</main>
