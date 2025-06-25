<script>
	import Button from './Button.svelte';
</script>

<section class="bg-light-coral relative overflow-hidden px-6 pt-16 pb-22">
	<img
		src="/assets/bg-pattern-home-6-about-5.svg"
		alt=""
		class="pointer-events-none absolute -bottom-4 left-0"
	/>

	<div
		class="relative z-10 mx-auto flex max-w-xl flex-col items-center gap-6 text-center md:flex-row md:justify-between"
	>
		<h2 class="text-sacramento-green text-[32px] font-bold">Ready to get started?</h2>
		<a href="/contact">
			<Button variant="primary" theme="dark">contact us</Button>
		</a>
	</div>
</section>
