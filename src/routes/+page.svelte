<script>
	import { Button } from '$lib/components/ui/button/index.js';
	import { fade, blur } from 'svelte/transition';
	import { onMount } from 'svelte';
	import { ChevronRight, Key, Telescope } from 'lucide-svelte';
	import Partners from '$lib/components/partners.svelte';
	import Testimonials from '$lib/components/testimonials.svelte';

	let mounted = false;
	onMount(() => {
		mounted = true;
	});
</script>

{#if mounted}
	<div class="mx-auto w-fit max-w-6xl px-3 sm:px-6">
		<h1
			class="text-center text-4xl font-semibold sm:text-5xl md:text-6xl"
			in:blur={{ delay: 50, duration: 300 }}
		>
			The <span
				class="bg-gradient-to-br from-[#CD31FF] to-fuchsia-700 bg-clip-text text-transparent"
				>BlockSprint</span
			>
			creates <br /> real business value.
		</h1>
		<p
			class="mt-5 max-w-2xl text-center text-base text-muted-foreground sm:text-lg md:text-xl"
			in:blur={{ delay: 50, duration: 400 }}
		>
			Empowering ambitious students and industry leaders to create impactful Web3 solutions. In
			3-month projects with innovative companies, students tackle exciting, real-world challenges.
		</p>
		<div class="mx-auto mt-5 grid w-fit gap-4 sm:flex" in:blur={{ delay: 50, duration: 500 }}>
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

	<div in:blur={{ delay: 50, duration: 600 }}>
		<Partners />
	</div>

	<div
		class="relative mx-auto mb-10 mt-32 grid max-w-6xl divide-y divide-zinc-800 border border-zinc-950 px-3 sm:px-6"
		in:blur={{ delay: 50, duration: 700 }}
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
					We bridge the gap between academia and the Industry by organizing Industry projects.
					Ambitious students tackle Web3 challenges and create value for our Industry partners.
					<br /><br />
					By fostering collaboration between academia and industry, we are accelerating Web3 innovation
					and empowering a new generation of builders.
				</p>
				<Button href="/about" class="w-fit text-sm" variant="secondary">About Us</Button>
			</div>
		</div>
		<div class="grid divide-zinc-800 sm:grid-cols-2 sm:divide-x">
			<div class="flex flex-col gap-5 p-4 sm:p-10">
				<h2 class="text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">Key Facts</h2>
				<p
					class="text grid max-w-md grid-cols-2 text-sm text-muted-foreground sm:text-base md:text-lg"
				>
					<span class="font-semibold">Start Date:</span>
					<span>April or October</span>

					<span class="font-semibold">Project Duration:</span>
					<span>3 months</span>

					<span class="font-semibold">Time Commitment:</span>
					<span>15–20 hours per week</span>

					<span class="font-semibold">Team Structure:</span>
					<span>2–4 students per project</span>

					<span class="font-semibold">Compensation:</span>
					<span>Up to €25 per hour</span>
				</p>
				<Button href="/projects" class="w-fit text-sm" variant="secondary">Projects</Button>
			</div>
			<div class="flex items-center justify-center p-4 sm:p-10">
				<Key class="h-56 w-56 text-zinc-800 sm:h-64 sm:w-64 md:h-72 md:w-72" strokeWidth=".25" />
			</div>
		</div>
	</div>

	<Testimonials />

	<div class="flex w-full items-center bg-gradient-to-b from-zinc-950 to-zinc-900">
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
					in:blur={{ delay: 50, duration: 800 }}
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
