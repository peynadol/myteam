<script lang="ts">
	import Button from './Button.svelte';
	import { toast } from 'svelte-sonner';

	let name = '';
	let email = '';
	let companyName = '';
	let title = '';
	let message = '';

	function handleSubmit(event: Event) {
		event.preventDefault();
		// show a toast on submission as it's not connected to a backend
		name = '';
		email = '';
		companyName = '';
		title = '';
		message = '';
		toast.success('Form submitted successfully!');
		console.log('Form submitted:', {
			name,
			email,
			companyName,
			title,
			message
		});
	}
</script>

<div class="relative overflow-hidden pb-20">
	<div class="mx-6 md:mx-30">
		<form on:submit={handleSubmit} class="flex flex-col gap-4 bg-none">
			<input
				type="text"
				placeholder="Name"
				bind:value={name}
				class="border-0 border-b border-white bg-transparent px-2 py-2 text-white placeholder-white/60 focus:border-white focus:outline-none"
			/>
			<input
				type="email"
				placeholder="Email"
				bind:value={email}
				class="border-0 border-b border-white bg-transparent px-2 py-2 text-white placeholder-white/60 focus:border-white focus:outline-none"
			/>
			<input
				type="text"
				placeholder="Company Name"
				bind:value={companyName}
				class="border-0 border-b border-white bg-transparent px-2 py-2 text-white placeholder-white/60 focus:border-white focus:outline-none"
			/>
			<input
				type="text"
				placeholder="Title"
				bind:value={title}
				class="border-0 border-b border-white bg-transparent px-2 py-2 text-white placeholder-white/60 focus:border-white focus:outline-none"
			/>
			<textarea
				placeholder="Message"
				bind:value={message}
				class="border-0 border-b border-white bg-transparent px-2 py-2 text-white placeholder-white/60 focus:border-white focus:outline-none"
				rows="4"
			></textarea>
			<div class="mt-4">
				<Button variant="secondary" theme="light" type="submit">submit</Button>
			</div>
		</form>
	</div>
	<img
		src="/assets/bg-pattern-contact-2.svg"
		alt="circular pattern"
		class="absolute right-0 bottom-0 translate-x-1/2 translate-y-1/2"
	/>
</div>
