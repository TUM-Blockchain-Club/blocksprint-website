<script>
	import deloitte from '$lib/img/deloitte.svg';
	import solanabeach from '$lib/img/solanabeach.svg';
	import wmdatenservice from '$lib/img/wmdatenservice.svg';
	import bosch from '$lib/img/bosch.svg';
	import { Button } from '$lib/components/ui/button/index.js';
	import { blur } from 'svelte/transition';
	import sührer from '$lib/img/sührer.jpeg';
	import albrecht from '$lib/img/albrecht.jpeg';
	import ducau from '$lib/img/ducau.jpeg';
	import busch from '$lib/img/busch.jpeg';

	const testimonials = [
		{
			companyLogo: bosch,
			companyName: 'Bosch',
			quote:
				'"We really enjoyed the professional setup and collaboration style of the TUM Blockchain Club to dive deeper in the decentralization technologies, which we identified as one of the hottest topics in the industry for the future!"',
			author: 'Peter Busch',
			position: 'Director Technology Management @ Bosch',
			image: busch
		},
		{
			companyLogo: wmdatenservice,
			companyName: 'WM Datenservice',
			quote:
				'"Participating in the BlockSprint was truly enriching - we learned so much from one another. The team exceeded my expectations, and I would highly recommend getting involved."',
			author: 'Dr. Duc Au',
			position: 'Head of WM Innovation Lab',
			image: ducau
		},
		{
			companyLogo: solanabeach,
			companyName: 'Solana Beach',
			quote:
				'"The industry initiative is a great way to kickoff a new project idea or build a prototype together with students. We enjoyed the simple process and easy communication."',
			author: 'Gustav Albrecht',
			position: 'CEO @ Solana Beach',
			image: albrecht
		},
		{
			companyLogo: deloitte,
			companyName: 'Deloitte',
			quote:
				'"Working with this team was a pleasure! They were motivated and organized. The project ran smoothly, and their dedication really showed. Highly recommend!"',
			author: 'Patrick Sührer',
			position: 'Senior Consultant @ Deloitte',
			image: sührer
		}
	];
</script>

<div
	class="mx-auto my-24 flex max-w-6xl flex-col px-3 sm:my-48 sm:px-6"
	in:blur={{ delay: 50, duration: 500 }}
>
	<h2 class="mb-1 text-center text-lg font-medium sm:text-xl md:text-2xl">Testimonials</h2>
	<p class="mx-auto max-w-2xl text-center text-sm text-muted-foreground sm:mb-10 md:text-base">
		What our partners say about us
	</p>
	<div class="grid grid-cols-1 gap-[1px] bg-zinc-900 sm:grid-cols-2">
		{#each testimonials as testimonial}
			<div class="items-left flex flex-col gap-10 bg-zinc-950 px-3 py-10 sm:p-10">
				<div class="flex w-fit">
					<img src={testimonial.companyLogo} alt={testimonial.companyName} class="h-6" />
				</div>
				<p class="text max-w-md text-[15px] italic text-muted-foreground">
					{testimonial.quote}
				</p>
				<div class="mt-auto flex items-center justify-between gap-4">
					<div class="flex flex-col space-y-0.5">
						<p class="font-medium">{testimonial.author}</p>
						<p class="text-sm text-muted-foreground">{testimonial.position}</p>
					</div>
					<img
						src={testimonial.image}
						alt={testimonial.author}
						class="h-12 w-12 rounded-full object-cover"
					/>
				</div>
			</div>
		{/each}
	</div>
</div>
