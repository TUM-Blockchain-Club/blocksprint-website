<script>
	import Navbar from '$lib/components/navbar.svelte';
	import { Button } from '$lib/components/ui/button/index.js';
	import { fade, blur } from 'svelte/transition';
	import { onMount } from 'svelte';
	import { on } from 'svelte/events';
	import bosch from '$lib/img/bosch.svg';
	import deloitte from '$lib/img/deloitte.svg';
	import solanabeach from '$lib/img/solanabeach.svg';
	import superteamgermany from '$lib/img/superteamgermany.svg';
	import wmdatenservice from '$lib/img/wmdatenservice.svg';
	import Marquee from 'svelte-fast-marquee';

	let mounted = false;
	onMount(() => {
		mounted = true;
	});
</script>

<header class="sticky mx-auto max-w-6xl p-8">
	<Navbar />
</header>

{#if mounted}
	<main class="w-full pt-20">
		<div class="mx-auto max-w-6xl px-11">
			<h1 class="text-6xl font-semibold" in:blur={{ delay: 200, duration: 300 }}>
				The <span
					class="bg-gradient-to-br from-[#CD31FF] to-fuchsia-500 bg-clip-text text-transparent"
					>Blocksprint</span
				>
				creates <br /> real business value.
			</h1>
			<p
				class="mt-5 max-w-2xl text-xl text-muted-foreground"
				in:blur={{ delay: 200, duration: 350 }}
			>
				We connect ambitious students with the industry. With our 3-month Blocksprints, we tackle
				exciting challenges in Web3.
			</p>
			<div class="mt-5 flex gap-4" in:blur={{ delay: 200, duration: 400 }}>
				<Button>Become a partner</Button>
				<Button variant="ghost">Join the Waitlist</Button>
			</div>
		</div>

		<div class="mx-auto mb-10 mt-32 max-w-6xl px-11" in:blur={{ delay: 200, duration: 450 }}>
			<h2 class="text-center text-xl font-medium">
				Former Project Partners <br /><span class="text-muted-foreground">
					From Startup to Enterprise - we got you.
				</span>
			</h2>
		</div>

		<Marquee gap="70px" speed={30}>
			<img src={bosch} alt="Bosch" class="mx-auto h-8" />
			<img src={wmdatenservice} alt="WM Datenservice" class="mx-auto h-8" />
			<img src={deloitte} alt="Deloitte" class="mx-auto h-8" />
			<img src={solanabeach} alt="Solanabeach" class="mx-auto h-8" />
			<img src={superteamgermany} alt="Superteam Germany" class="mx-auto h-8" />
		</Marquee>
	</main>
{/if}
