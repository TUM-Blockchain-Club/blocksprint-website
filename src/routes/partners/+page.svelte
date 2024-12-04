<script>
	import Footer from '$lib/components/footer.svelte';
	import Partners from '$lib/components/partners.svelte';
	import { blur } from 'svelte/transition';
	import {
		ChevronRight,
		Key,
		Telescope,
		Users,
		Award,
		Phone,
		Briefcase,
		Handshake,
		Target,
		Blocks
	} from 'lucide-svelte';
	import { Button } from '$lib/components/ui/button/index.js';
	import tbc from '$lib/img/tbc.svg';
	import Faq from '$lib/components/faq.svelte';

	let benefits = [
		{
			title: 'Highly Qualified Team',
			description:
				'We ensure that the selected participants are qualified to make the project a full success.',
			icon: Users
		},
		{
			title: 'Marketing and Employer Branding',
			description:
				'We attract the best talent through dedicated marketing and position your company as a leader in Web3.',
			icon: Award
		},
		{
			title: 'Continuous Project Support',
			description:
				'There will be one dedicated project mentor from TBC who will moderate weekly calls and help if needed.',
			icon: Phone
		},
		{
			title: 'Future Employment Potential',
			description: 'Identify potential hires among top-performing students from TUM.',
			icon: Briefcase
		},
		{
			title: 'Networking Events',
			description:
				'We organize team building, kick-off, mid-term, and final pitch events and invite the Munich Web3 community.',
			icon: Handshake
		},
		{
			title: 'Milestones & Goals',
			description:
				'We define milestones and a project goal to ensure that all stakeholders are on the same page.',
			icon: Target
		}
	];
</script>

<div
	class="mx-auto grid max-w-6xl gap-10 divide-zinc-800 px-3 pt-10 sm:grid-cols-2 sm:px-6"
	in:blur={{ delay: 50, duration: 300 }}
>
	<div class="order-1 flex flex-col gap-5 sm:order-2">
		<h2 class="text-2xl font-semibold text-foreground sm:text-3xl md:text-4xl">BlockSprint</h2>
		<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
			Ambitious students work on a Web3-related problem provided by you, delivering high-quality,
			innovative solutions. You just need to define the project idea, we handle participant
			selection, team organization and management. Let's create an impact together!
		</p>
		<Button href="/projects" class="w-fit text-sm" variant="secondary">Become a Partner</Button>
	</div>
	<div class="order-2 mx-auto flex items-center justify-center sm:order-1">
		<Blocks class="h-56 w-56 text-zinc-800 sm:h-64 sm:w-64 md:h-72 md:w-72" strokeWidth=".25" />
	</div>
</div>

<div in:blur={{ delay: 50, duration: 400 }}>
	<Partners />
</div>

<div
	class="mx-auto my-48 flex max-w-6xl flex-col px-3 sm:px-6"
	in:blur={{ delay: 50, duration: 500 }}
>
	<h2 class="mb-10 text-center text-base font-medium sm:text-lg md:text-xl">
		Partner Benefits <br /><span class="text-muted-foreground">Lorem Ipsum</span>
	</h2>
	<div class="grid grid-cols-1 gap-[1px] bg-zinc-900 sm:grid-cols-2 lg:grid-cols-3">
		{#each benefits as benefit}
			<div class="items-left flex h-48 flex-col justify-between bg-zinc-950 p-9">
				<div class="flex h-fit items-center justify-between">
					<p class="text-xl font-medium">
						{benefit.title}
					</p>
					<div class="flex h-11 w-11 items-center justify-center rounded-full">
						<benefit.icon class="mx-auto h-6 w-6 text-zinc-50" />
					</div>
				</div>
				<p class="text-xs text-muted-foreground sm:text-sm">
					{benefit.description}
				</p>
			</div>
		{/each}
	</div>
</div>

<Faq category="partners" />
