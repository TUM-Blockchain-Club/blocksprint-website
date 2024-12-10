<script>
	import deloitte from '$lib/img/deloitte.svg';
	import solanabeach from '$lib/img/solanabeach.svg';
	import { Button } from '$lib/components/ui/button/index.js';
	import { blur } from 'svelte/transition';
	import sührer from '$lib/img/sührer.jpeg';
	import albrecht from '$lib/img/albrecht.jpeg';
</script>

<div
	class="mx-auto my-24 flex max-w-6xl flex-col px-3 sm:my-48 sm:px-6"
	in:blur={{ delay: 50, duration: 500 }}
>
	<h2 class="mb-1 text-center text-lg font-medium sm:text-xl md:text-2xl">Testimonials</h2>
	<p class="mx-auto mb-10 max-w-2xl text-center text-sm text-muted-foreground md:text-base">
		What our partners say about us
	</p>
	<div class="grid grid-cols-1 gap-[1px] bg-zinc-900 sm:grid-cols-2">
		<div class="items-left flex flex-col gap-10 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<img src={deloitte} alt="Deloitte" class="h-6" />
			</div>
			<p class="text max-w-md text-[15px] italic text-muted-foreground">
				"Working with this team was a pleasure! They were motivated and organized. The project ran
				smoothly, and their dedication really showed. Highly recommend!"
			</p>
			<div class="mt-auto flex items-center justify-between gap-4">
				<div class="flex flex-col space-y-0.5">
					<p class="font-medium">Patrick Sührer</p>
					<p class="text-sm text-muted-foreground">
						Senior Consultant @ Deloitte Blockchain Institute
					</p>
				</div>
				<img src={sührer} alt="Sührer" class="h-12 w-12 rounded-full object-cover" />
			</div>
		</div>

		<div class="items-left flex flex-col gap-10 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<img src={solanabeach} alt="Solana Beach" class="h-6" />
			</div>
			<p class="text max-w-md text-[15px] italic text-muted-foreground">
				"The industry initiative is a great way to kickoff a new project idea or build a prototype
				together with students. We enjoyed the simple process and easy communication."
			</p>
			<div class="mt-auto flex items-center justify-between gap-4">
				<div class="flex flex-col space-y-0.5">
					<p class="font-medium">Gustav Albrecht</p>
					<p class="text-sm text-muted-foreground">CEO @ Solana Beach</p>
				</div>
				<img src={albrecht} alt="Albrecht" class="h-12 w-12 rounded-full object-cover" />
			</div>
		</div>
	</div>
</div>
