<script lang="ts">
	import Seo from '$lib/components/ui/SEO.svelte';
	import '../app.css';
	import { ModeWatcher } from 'mode-watcher';
	let { children } = $props();
</script>

<Seo />
<ModeWatcher />
{@render children()}
