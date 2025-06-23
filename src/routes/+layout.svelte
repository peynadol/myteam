<script lang="ts">
	import '../app.css';
	import '@fontsource/livvic/700.css';
	import '@fontsource/livvic/600.css';
	import '@fontsource/livvic/400.css';
	import Nav from '$lib/components/Nav.svelte';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();
</script>

<div class="bg-midnight-green min-h-screen text-white">
	<Nav />

	{@render children()}
	<Footer />
</div>
