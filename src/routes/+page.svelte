<script>
	import { Button } from '$lib/components/ui/button/index.js';
	import { fade, blur } from 'svelte/transition';
	import { onMount } from 'svelte';
	import { ChevronRight, Key, Telescope } from 'lucide-svelte';
	import Partners from '$lib/components/partners.svelte';

	let mounted = false;
	onMount(() => {
		mounted = true;
	});
</script>

{#if mounted}
	<div class="mx-auto max-w-6xl px-3 sm:px-6">
		<h1
			class="text-center text-4xl font-semibold sm:text-left sm:text-5xl md:text-6xl"
			in:blur={{ delay: 200, duration: 300 }}
		>
			The <span
				class="bg-gradient-to-br from-[#CD31FF] to-fuchsia-700 bg-clip-text text-transparent"
				>BlockSprint</span
			>
			creates <br /> real business value.
		</h1>
		<p
			class="mt-5 max-w-2xl text-center text-base text-muted-foreground sm:text-left sm:text-lg md:text-xl"
			in:blur={{ delay: 200, duration: 350 }}
		>
			Empowering ambitious students and industry leaders to build a thriving Web3 community of
			builders. Through 3-month projects with innovative companies, students tackle exciting
			challenges.
		</p>
		<div
			class="mx-auto mt-5 grid w-fit gap-4 sm:mx-0 sm:flex"
			in:blur={{ delay: 200, duration: 400 }}
		>
			<Button href="https://apply.tum-blockchain.com/industry-partner">Become a partner</Button>
			<Button
				href="https://apply.tum-blockchain.com/industry-student-waitlist"
				variant="ghost"
				class="flex gap-1"
			>
				<p class="bg-gradient-to-r from-zinc-50 to-zinc-400 bg-clip-text text-transparent">
					Join the Waitlist
				</p>
				<ChevronRight class="h-5 w-5" />
			</Button>
		</div>
	</div>

	<div in:blur={{ delay: 200, duration: 450 }}>
		<Partners />
	</div>

	<div
		class="relative mx-auto mb-10 mt-32 grid max-w-6xl divide-y divide-zinc-800 border border-zinc-950 px-3 sm:px-6"
		in:blur={{ delay: 200, duration: 550 }}
	>
		<div class="grid- grid divide-zinc-800 sm:grid-cols-2 sm:divide-x">
			<div class="order-2 flex items-center justify-center p-4 sm:order-1 sm:p-10">
				<Telescope
					class="h-56 w-56 text-zinc-800 sm:h-64 sm:w-64 md:h-72 md:w-72"
					strokeWidth=".25"
				/>
			</div>
			<div class="order-1 flex flex-col gap-5 p-4 sm:order-2 sm:p-10">
				<h2 class="text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">Our Vision</h2>
				<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
					Through BlockSprint projects, we bridge the gap between theoretical education and the
					practical use of Web3 technologies. These projects empower students to tackle real-world
					challenges presented by industry partners.
					<br /><br />
					By fostering collaboration between academia and industry, we drive innovation within the Web3
					ecosystem: companies unlock groundbreaking solutions, and students emerge as the next generation
					of Web3 leaders with hands-on experience and deep industry insights.
				</p>
				<Button href="/about" class="w-fit text-sm" variant="secondary">About Us</Button>
			</div>
		</div>
		<div class="grid divide-zinc-800 sm:grid-cols-2 sm:divide-x">
			<div class="flex flex-col gap-5 p-4 sm:p-10">
				<h2 class="text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">Key Factors</h2>
				<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
					Start Date: Beginning of each semester
					<br />
					Project Duration: 3 months
					<br />
					Time Commitment: 15–20 hours per week
					<br />
					Team Structure: 2–4 students per project
					<br />
					Compensation: Up to €25 per hour
				</p>
				<Button href="/projects" class="w-fit text-sm" variant="secondary">Projects</Button>
			</div>
			<div class="flex items-center justify-center p-4 sm:p-10">
				<Key class="h-56 w-56 text-zinc-800 sm:h-64 sm:w-64 md:h-72 md:w-72" strokeWidth=".25" />
			</div>
		</div>
	</div>

	<div
		class="mt-16 flex w-full items-center bg-gradient-to-b from-zinc-950 to-zinc-900 sm:mt-20 md:mt-24"
	>
		<div
			class="mx-auto my-auto flex w-full max-w-6xl flex-col justify-between gap-8 px-3 py-16 sm:px-6 sm:py-20 md:flex-row md:py-24"
		>
			<p class="text-center text-4xl font-semibold sm:text-5xl md:text-left md:text-6xl">
				Ready to join <br />
				and partner up?
			</p>
			<div class="mx-auto flex flex-col justify-between md:mx-0">
				<div></div>
				<div
					class="mx-auto grid w-fit gap-4 sm:mx-0 sm:flex"
					in:blur={{ delay: 200, duration: 400 }}
				>
					<Button href="https://apply.tum-blockchain.com/industry-partner">Become a partner</Button>
					<Button
						href="https://apply.tum-blockchain.com/industry-student-waitlist"
						variant="ghost"
						class="flex gap-1"
					>
						<p class="bg-gradient-to-r from-zinc-50 to-zinc-400 bg-clip-text text-transparent">
							Join the Waitlist
						</p>
						<ChevronRight class="h-5 w-5" />
					</Button>
				</div>
			</div>
		</div>
	</div>
{/if}
