<script lang="ts" context="module">
	export const DEFAULT_SHEET_SIZE = '7x5cm';
</script>

<script lang="ts">
	export let value = DEFAULT_SHEET_SIZE;
</script>

<select bind:value>
	<option value="7x5cm">7x5cm</option>
</select>
