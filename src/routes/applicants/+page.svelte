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
		Blocks,
		GraduationCap,
		HandCoins,
		PocketKnife,
		Rocket
	} from '@lucide/svelte';
	import { Button } from '$lib/components/ui/button/index.js';
	import tbc from '$lib/img/tbc.svg';
	import Faq from '$lib/components/faq.svelte';
	import Timeline from '$lib/components/timeline.svelte';
	import { onMount } from 'svelte';
	let milestones = [
		{
			date: 'Sep 09, 2025',
			title: 'Application Period Opens'
		},
		{
			date: 'Sep 21, 2025',
			title: 'Application Period Closes'
		},
		{
			date: 'Oct 24, 2025',
			title: 'Kick-off Event'
		},
		{
			date: 'Dec 05, 2025',
			title: 'Mid-term Presentations'
		},
		{
			date: 'Jan 16, 2026',
			title: 'Final Presentations'
		}
	];

	let benefits = [
		{
			title: 'Exciting Web3 Challenges',
			description: 'Get the opportunity to work on real challenges in the Web3 ecosystem.',
			icon: Rocket
		},
		{
			title: 'Web3 Industry Insights',
			description:
				'Work with leading Web3 companies and get first-hand insights into the groundbreaking blockchain industry.',
			icon: Telescope
		},
		{
			title: 'Highly competitive Salary',
			description:
				'Your work for the project will be compensated fairly. The salary depends on the project but is ensured to be well above average.',
			icon: HandCoins
		},
		{
			title: 'Meet ambitious People',
			description:
				'Build relationships with like-minded students that want to push boundaries in Web3.',
			icon: Users
		},
		{
			title: 'Expand your Skillset',
			description:
				'Grow together as a team and explore the use of cutting-edge tech in production. Apply your theoretical knowledge in practice.',
			icon: PocketKnife
		},
		{
			title: 'Employment Opportunity',
			description:
				'Impress our partners with your contribution and you will have the opportunity to get employed by the partner company.',
			icon: Briefcase
		}
	];

	let mounted = false;
	let gradientAngle = 0;

	onMount(() => {
		mounted = true;

		// Set up the animation loop for the gradient rotation
		const animateGradient = () => {
			gradientAngle = (gradientAngle + 1) % 360;
			requestAnimationFrame(animateGradient);
		};

		// Start the animation
		const animation = requestAnimationFrame(animateGradient);

		// Clean up on component unmount
		return () => {
			cancelAnimationFrame(animation);
		};
	});
</script>

<div
	class="mx-auto grid max-w-6xl gap-10 px-3 pb-32 pt-10 sm:grid-cols-2 sm:px-6"
	in:blur={{ delay: 50, duration: 300 }}
>
	<div class="order-1 flex flex-col gap-5 sm:order-2">
		<h2 class="text-2xl font-semibold text-foreground sm:text-3xl md:text-4xl">BlockSprint</h2>
		<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
			Work with leading Web3 companies to solve real-world challenges in a 3-month BlockSprint
			project. Gain hands-on experience, build your blockchain expertise and earn a competitive
			salary!
		</p>
		<Button
			href="https://apply.tum-blockchain.com/talent-pool"
			class="w-fit text-sm"
			variant="secondary">Join our Talent Pool</Button
		>
	</div>
	<div class="order-2 flex items-center justify-center sm:order-1">
		<GraduationCap
			class="h-56 w-56 text-zinc-800 sm:h-64 sm:w-64 md:h-72 md:w-72"
			strokeWidth=".25"
		/>
	</div>
</div>

<div in:blur={{ delay: 50, duration: 400 }}>
	<Timeline
		{milestones}
		tag="Upcoming"
		title="Timeline"
		subtitle="Events and deadlines for the next BlockSprint iteration"
	/>
</div>

<div
	class="mx-auto my-24 flex max-w-6xl flex-col px-3 sm:my-48 sm:px-6"
	in:blur={{ delay: 50, duration: 500 }}
>
	<div class="grid grid-cols-1 gap-[1px] bg-zinc-900 sm:grid-cols-2">
		<div class="flex flex-col gap-5 bg-zinc-950 p-5 sm:p-10">
			<h2 class="pt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				General Information
			</h2>
			<div class="flex flex-col gap-2">
				<ul class="list-disc pl-4 text-sm text-muted-foreground sm:text-base">
					<li>Start: Beginning of each semester (October - April)</li>
					<li>Duration: 3 months</li>
					<li>Commitment: 15-20h per week</li>
					<li>Teams: 2-4 students per project</li>
					<li>Compensation: highly competitive</li>
					<li>Application: starting 9th September 2025</li>
				</ul>
			</div>
		</div>

		<div class="flex flex-col gap-5 bg-zinc-950 p-5 sm:p-10">
			<h2 class="pt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				General Requirements
			</h2>
			<div class="flex flex-col gap-2">
				<ul class="list-disc pl-4 text-sm text-muted-foreground md:text-base">
					<li>You are a student enrolled at a university</li>
					<li>You have general knowledge and interest in blockchain technology</li>
					<li>You are a team player</li>
					<li>
						You have followed TUM Blockchain Club's <a
							href="https://www.instagram.com/tumblockchain/"
							target="_blank"
							rel="noopener"
							class="text-muted-foreground hover:underline">Instagram</a
						>,
						<a
							href="https://www.linkedin.com/company/tum-blockchain-club/"
							target="_blank"
							rel="noopener"
							class="text-muted-foreground hover:underline">LinkedIn</a
						>
						and
						<a
							href="https://x.com/tbc_munich"
							target="_blank"
							rel="noopener"
							class="text-muted-foreground hover:underline">X</a
						> 😉
					</li>
				</ul>
			</div>
		</div>
	</div>
</div>

<div
	class="mx-auto my-24 flex max-w-6xl flex-col px-3 sm:my-48 sm:px-6"
	in:blur={{ delay: 50, duration: 600 }}
>
	<h2 class="mb-1 text-center text-lg font-medium sm:text-xl md:text-2xl">Opportunities</h2>
	<p class="mx-auto mb-10 max-w-2xl text-center text-sm text-muted-foreground md:text-base">
		With Industry Projects you can dive deep into the Web3 ecosystem and get to know the latest
		blockchain technologies first-hand. You will be able to experience how Web3 companies function
		from the inside and work on cutting-edge problems.
	</p>
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
				<p class="text-sm text-muted-foreground">
					{benefit.description}
				</p>
			</div>
		{/each}
	</div>
</div>

<Faq category="students" />
