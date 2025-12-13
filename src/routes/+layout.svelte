<script lang="ts">

    import { onMount } from 'svelte';
    import { injectSpeedInsights } from '@vercel/speed-insights/sveltekit';

	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();

	    onMount(() => {
        injectSpeedInsights();
    });
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children?.()}
