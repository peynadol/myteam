<script>
	import Icon from '@iconify/svelte';
	export let isOpen = false;
	export let close;
</script>

<div
	class="fixed inset-0 z-50 bg-black/50 transition-opacity duration-300 {isOpen
		? 'opacity-100'
		: 'pointer-events-none opacity-0'}"
	on:click={close}
	on:keydown={(e) => e.key === 'Escape' && close()}
	role="button"
	tabindex="0"
	aria-label="Close sheet"
>
	<div
		class="bg-police-blue absolute top-0 right-0 flex h-full w-[60%] max-w-lg flex-col justify-between p-6 text-white shadow-lg transition-transform duration-300 ease-in-out {isOpen
			? 'translate-x-0'
			: 'translate-x-full'}"
		on:click|stopPropagation
		on:keydown|stopPropagation
		role="dialog"
		aria-modal="true"
		aria-labelledby="sheet-title"
		tabindex="-1"
	>
		<div class="flex justify-end">
			<button on:click={close} aria-label="Close menu">
				<Icon icon="iconamoon:close-bold" class="h-8 w-8" />
			</button>
		</div>

		<nav class="mt-10 ml-4 flex flex-col items-start gap-6 text-xl" aria-label="Main navigation">
			<h2 id="sheet-title" class="sr-only">Navigation Menu</h2>
			<a href="/" on:click={close} class="font-semibold hover:underline">home</a>
			<a href="/about" on:click={close} class="font-semibold hover:underline">about</a>
			<a
				href="/contact"
				on:click={close}
				class="hover:text-dark-teal mt-4 rounded-full border-2 px-6 py-3 font-bold text-white hover:bg-white"
			>
				contact us
			</a>
		</nav>

		<div class="mt-auto flex justify-center pt-12">
			<img src="/assets/bg-pattern-about-1-mobile-nav-1.svg" alt="MyTeam Logo" class="" />
		</div>
	</div>
</div>
