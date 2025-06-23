<script>
	export let name;
	export let title;
	export let imageSrc;
</script>

<div class="bg-sacramento-green relative mx-6 p-6 text-center">
	<img
		src={imageSrc}
		alt={name}
		class="mx-auto mb-4 h-24 w-24 rounded-full border-2 border-white"
	/>
	<h3 class="text-rapture-blue text-lg font-bold">{name}</h3>
	<p class="mb-8 text-white italic">{title}</p>

	<button
		class="bg-light-coral text-deep-jungle-green absolute -bottom-7 left-1/2 inline-flex h-14 w-14 -translate-x-1/2 items-center justify-center rounded-full text-[32px] font-bold"
		aria-label="Show more"
	>
		<img src="/assets/icon-cross.svg" alt="plus symbol" />
	</button>
</div>
