<script lang="ts">
	import { browser } from '$app/env';

	import { onMount } from 'svelte';

	let ready = false;

	onMount(() => {
		if (browser) {
			ready = true;
		}
	});
</script>

{#if ready}
	<webview
		id="foo"
		src="https://www.baidu.com/"
		style="display:inline-block; width:640px; height:480px"
	/>
{/if}
demo
