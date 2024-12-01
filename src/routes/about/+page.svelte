<script>
	import Footer from '$lib/components/footer.svelte';
	import { ChevronRight, Key, Telescope } from 'lucide-svelte';
	import { Button } from '$lib/components/ui/button/index.js';
	import tbc from '$lib/img/tbc.svg';

	let members = [
		{
			image: tbc,
			name: 'Jakob Isermann',
			linkedin: 'https://www.linkedin.com/in/jis3r/'
		},
		{
			image: tbc,
			name: 'Jakob Isermann',
			linkedin: 'https://www.linkedin.com/in/jis3r/'
		},
		{
			image: tbc,
			name: 'Jakob Isermann',
			linkedin: 'https://www.linkedin.com/in/jis3r/'
		},
		{
			image: tbc,
			name: 'Jakob Isermann',
			linkedin: 'https://www.linkedin.com/in/jis3r/'
		},
		{
			image: tbc,
			name: 'Jakob Isermann',
			linkedin: 'https://www.linkedin.com/in/jis3r/'
		},
		{
			image: tbc,
			name: 'Jakob Isermann',
			linkedin: 'https://www.linkedin.com/in/jis3r/'
		},
		{
			image: tbc,
			name: 'Jakob Isermann',
			linkedin: 'https://www.linkedin.com/in/jis3r/'
		},
		{
			image: tbc,
			name: 'Jakob Isermann',
			linkedin: 'https://www.linkedin.com/in/jis3r/'
		},
		{
			image: tbc,
			name: 'Jakob Isermann',
			linkedin: 'https://www.linkedin.com/in/jis3r/'
		},
		{
			image: tbc,
			name: 'Jakob Isermann',
			linkedin: 'https://www.linkedin.com/in/jis3r/'
		},
		{
			image: tbc,
			name: 'Jakob Isermann',
			linkedin: 'https://www.linkedin.com/in/jis3r/'
		},
		{
			image: tbc,
			name: 'Jakob Isermann',
			linkedin: 'https://www.linkedin.com/in/jis3r/'
		}
	];
</script>

<div class="grid- grid divide-zinc-800 sm:grid-cols-2">
	<div class="order-2 flex items-center justify-center p-4 sm:order-1 sm:p-10">
		<Telescope class="h-56 w-56 text-zinc-800 sm:h-64 sm:w-64 md:h-72 md:w-72" strokeWidth=".25" />
	</div>
	<div class="order-1 flex flex-col gap-5 p-4 sm:order-2 sm:p-10">
		<h2 class="text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">Our Vision</h2>
		<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
			Through BlockSprint projects, we bridge the gap between theoretical education and the
			practical use of Web3 technologies. These projects empower students to tackle real-world
			challenges presented by industry partners.
			<br /><br />
			By fostering collaboration between academia and industry, we drive innovation within the Web3 ecosystem:
			companies unlock groundbreaking solutions, and students emerge as the next generation of Web3 leaders
			with hands-on experience and deep industry insights.
		</p>
	</div>
</div>

<div class="mx-auto mt-32 flex max-w-6xl flex-col px-3 sm:px-6">
	<h2 class="mb-10 text-center text-base font-medium sm:text-lg md:text-xl">
		BlockSprint Team <br /><span class="text-muted-foreground">Lorem</span>
	</h2>
	<div class="grid grid-cols-1 gap-8 sm:grid-cols-2 md:grid-cols-4 lg:gap-12">
		{#each members as member}
			<div class="items-left flex flex-col justify-center p-4">
				<img src={member.image} alt={member.name} class="w-full rounded-lg" />
				<p class="mt-4 text-foreground sm:text-lg md:text-xl">{member.name}</p>
				<a
					href={member.linkedin}
					target="_blank"
					rel="noopener noreferrer"
					class="text-sm text-muted-foreground hover:underline">LinkedIn</a
				>
			</div>
		{/each}
	</div>
</div>
