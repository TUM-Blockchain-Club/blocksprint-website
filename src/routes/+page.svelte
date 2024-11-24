<script>
	import Navbar from '$lib/components/navbar.svelte';
	import { Button } from '$lib/components/ui/button/index.js';
	import { fade, blur } from 'svelte/transition';
	import { onMount } from 'svelte';
	import { on } from 'svelte/events';

	let mounted = false;
	onMount(() => {
		mounted = true;
	});
</script>

<header class="sticky mx-auto max-w-6xl p-8">
	<Navbar />
</header>

{#if mounted}
	<main class="mx-auto max-w-6xl px-11 pt-20">
		<h1 class="text-6xl font-semibold" in:blur={{ delay: 200, duration: 300 }}>
			The <span
				class="bg-gradient-to-br from-[#CD31FF] to-fuchsia-500 bg-clip-text text-transparent"
				>Blocksprint</span
			>
			creates <br /> real business value.
		</h1>
		<p class="mt-5 max-w-2xl text-xl text-muted-foreground" in:blur={{ delay: 200, duration: 350 }}>
			We connect ambitious students with the industry. With our 3-month Blocksprints, we tackle
			exciting challenges in Web3.
		</p>
		<div class="mt-5 flex gap-4" in:blur={{ delay: 200, duration: 400 }}>
			<Button>Become a partner</Button>
			<Button variant="ghost">Join the Waitlist</Button>
		</div>

		<div class="mt-32" in:blur={{ delay: 200, duration: 450 }}>
			<h2 class="text-center text-3xl font-semibold">Former Project Partners</h2>
			<p class="mx-auto mt-5 max-w-2xl text-center text-lg text-muted-foreground">
				Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
				labore et dolore magna aliqua.
			</p>
		</div>
	</main>
{/if}
