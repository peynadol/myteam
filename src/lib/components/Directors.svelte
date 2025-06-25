<script>
	import DirectorCard from './DirectorCard.svelte';
	import QuoteCard from './QuoteCard.svelte';
</script>

<section class="bg-deep-jungle-green relative overflow-hidden">
	<img
		src="assets/bg-pattern-about-2-contact-1.svg"
		alt="circle logo"
		class="pointer-events-none absolute top-0 h-auto -translate-x-1/2 -translate-y-[100px]"
	/>
	<h2 class="mt-20 mb-10 text-center text-[32px] font-bold">Meet the directors</h2>
	<div class="flex flex-col gap-15 md:grid md:grid-cols-2 md:gap-x-0 md:px-16 lg:grid-cols-3">
		<DirectorCard imageSrc="/assets/avatar-nikita.jpg" name="Nikita Marks" title="Founder & CEO" />
		<DirectorCard
			imageSrc="/assets/avatar-christian.jpg"
			name="Christian Duncan"
			title="Co-founder & COO"
		/>
		<DirectorCard imageSrc="/assets/avatar-cruz.jpg" name="Cruz Hamer" title="Co-founder & CMO" />
		<DirectorCard
			imageSrc="/assets/avatar-drake.jpg"
			name="Drake Johnson"
			title="Business Development Lead"
		/>
		<DirectorCard
			imageSrc="/assets/avatar-griffin.jpg"
			name="Griffin Wise"
			title="Lead Marketing"
		/>
		<QuoteCard
			name="Aden Allan"
			message="“Empowered teams create truly amazing products. Set the north star and let them follow it.”"
		/>
	</div>
	<div class="mt-4 flex justify-end">
		<img src="/assets/bg-pattern-home-4-about-3.svg" alt="square icon" />
	</div>
</section>
