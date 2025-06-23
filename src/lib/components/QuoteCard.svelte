<script>
	export let name;
	export let message;
</script>

<div class="bg-sacramento-green relative mx-6 p-6 text-center">
	<h3 class="text-rapture-blue text-lg font-bold">{name}</h3>
	<p class="mb-8 text-white italic">{message}</p>
	<div class="mb-6 flex justify-center gap-4">
		<img src="assets/icon-twitter.svg" alt="twitter icon" />
		<img src="assets/icon-linkedin.svg" alt="linkedin icon" />
	</div>

	<button
		class="bg-rapture-blue text-deep-jungle-green absolute -bottom-7 left-1/2 inline-flex h-14 w-14 -translate-x-1/2 items-center justify-center rounded-full text-[32px] font-bold"
		aria-label="Show more"
	>
		<img src="/assets/icon-cross.svg" alt="plus symbol" />
	</button>
</div>
