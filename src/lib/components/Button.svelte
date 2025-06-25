<script lang="ts">
	import clsx from 'clsx';

	export let type: 'button' | 'submit' | 'reset' = 'button';
	export let variant: 'primary' | 'secondary' = 'primary';
	export let theme: 'light' | 'dark' = 'light';
	export let disabled = false;
</script>

<button
	{type}
	{disabled}
	{...$$restProps}
	class={clsx(
		'rounded-full border-2 px-6 py-2 text-[18px] font-semibold tracking-wide transition-colors duration-200',
		disabled ? 'cursor-not-allowed' : 'cursor-pointer',

		// Primary Light
		variant === 'primary' &&
			theme === 'light' &&
			(disabled
				? 'bg-sacramento-green border-white/30 text-white/30'
				: 'hover:text-sacramento-green border-white bg-none text-white hover:bg-white'),

		// Primary Dark
		variant === 'primary' &&
			theme === 'dark' &&
			(disabled
				? 'border-black/30 bg-white text-black/30'
				: 'border-sacramento-green text-sacramento-green hover:bg-sacramento-green bg-none hover:text-white'),

		// Secondary Light
		variant === 'secondary' &&
			theme === 'light' &&
			(disabled
				? 'bg-[#416367]'
				: 'text-sacramento-green border-sacramento-green hover:bg-rapture-blue bg-white')
	)}
>
	<slot />
</button>
