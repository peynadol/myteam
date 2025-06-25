<script lang="ts">
	import '../app.css';
	import '@fontsource/livvic/700.css';
	import '@fontsource/livvic/600.css';
	import '@fontsource/livvic/400.css';
	import Nav from '$lib/components/Nav.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import MobileMenu from '$lib/components/MobileMenu.svelte';
	let isOpen = false;
	export let children;
</script>

<div class="bg-midnight-green min-h-screen text-white">
	<Nav on:open={() => (isOpen = true)} />
	<MobileMenu {isOpen} close={() => (isOpen = false)} />
	{@render children()}
	<Footer />
</div>
