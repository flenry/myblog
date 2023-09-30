<script lang="ts">
	import { navigating } from '$app/stores';
	import { fade } from 'svelte/transition';

	export let url = '';
</script>

{#key url}
	<div class="transition" in:fade>
		<slot />
	</div>
{/key}

<style>
	.transition {
		height: 100%;
	}
</style>
