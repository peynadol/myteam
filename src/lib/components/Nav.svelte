<script>
	import { createEventDispatcher } from 'svelte';
	import Icon from '@iconify/svelte';
	import Button from './Button.svelte';

	const dispatch = createEventDispatcher();
</script>

<div class="bg-midnight-green flex items-center justify-between px-6 py-6 md:py-14">
	<div class="flex items-center gap-6">
		<a href="/">
			<img src="/assets/logo.svg" alt="Logo" class="h-8" />
		</a>

		<div class="hidden items-center gap-10 text-[18px] font-semibold md:ml-4 md:flex">
			<a href="/">home</a>
			<a href="/about">about</a>
		</div>
	</div>

	<div class="hidden md:block">
		<a href="/contact"><Button variant="primary">contact us</Button></a>
	</div>

	<button on:click={() => dispatch('open')} aria-label="Open menu" class="block md:hidden">
		<Icon icon="iconamoon:menu-burger-horizontal-bold" class="h-8 w-8" />
	</button>
</div>
