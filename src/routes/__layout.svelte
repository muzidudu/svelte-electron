<script lang="ts">
	import { onMount } from 'svelte';

	let ready: boolean = false;
	onMount(() => (ready = true));
</script>
<div class="dragbar"></div>	
<div style="padding-top: 40px;">
	<nav>
		<li><a href="/">home</a></li>
		<li><a href="/demo">demo</a></li>
	</nav>
</div>

{#if ready}
	<slot />
{/if}

<style>
	.dragbar {
		-webkit-app-region: drag;
		position: absolute;
		z-index: 100;
		height: 30px;
		width: 100%;
	}
</style>
