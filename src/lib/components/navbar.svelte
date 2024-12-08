<script>
	import { Button } from '$lib/components/ui/button/index.js';
	import { scramble } from '$lib/utils/scramble.js';
	import tbc from '$lib/img/tbc.svg';
	import { Menu, X } from 'lucide-svelte';
	import { goto } from '$app/navigation';
	import { page } from '$app/stores';
	import { onMount } from 'svelte';
	import { text } from '@sveltejs/kit';

	let menuOpen = $state(false);
	let currentPage = $state('');

	$effect(() => {
		document.body.style.overflow = menuOpen ? 'hidden' : '';
	});

	$effect(() => {
		currentPage = $page.url.pathname;
	});

	onMount(() => {
		currentPage = $page.url.pathname;
	});
</script>

<header
	class:h-dvh={menuOpen}
	class:pb-5={menuOpen}
	class="fixed top-0 z-50 w-full bg-zinc-950 bg-opacity-60 px-3 pt-5 backdrop-blur-xl md:px-5"
>
	<nav
		class:h-full={menuOpen}
		class="z-50 mx-auto h-12 w-full rounded-2xl border border-zinc-800 px-3 py-2 transition-all duration-300 sm:max-w-6xl"
	>
		<div class="flex w-full items-center justify-between">
			<a href="/" class="flex items-center justify-center gap-2">
				<img src={tbc} alt="TUM Blockchain Club" class="h-7 w-7" />
				<p class="hidden text-foreground sm:flex">TUM BLOCKCHAIN CLUB</p>
			</a>

			<div class="flex gap-4 lg:gap-8">
				<div class="hidden items-center gap-4 text-sm md:flex lg:gap-8">
					<a
						href="/projects"
						class:text-foreground={currentPage.endsWith('/projects')}
						class:text-muted-foreground={!currentPage.endsWith('/projects')}
						class="w-[53px] overflow-hidden whitespace-nowrap hover:text-foreground"
						id="Projects"
						onmouseenter={() => {
							scramble('Projects', 'Projects');
						}}
						onmouseleave={() => (document.getElementById('Projects').innerText = 'Projects')}
					>
						Projects
					</a>
					<a
						href="/applicants"
						class:text-foreground={currentPage.endsWith('/applicants')}
						class:text-muted-foreground={!currentPage.endsWith('/applicants')}
						class="w-[68px] overflow-hidden whitespace-nowrap hover:text-foreground"
						id="Applicants"
						onmouseenter={() => {
							scramble('Applicants', 'Applicants');
						}}
						onmouseleave={() => (document.getElementById('Applicants').innerText = 'Applicants')}
					>
						Applicants
					</a>
					<a
						href="/partners"
						class:text-foreground={currentPage.endsWith('/partners')}
						class:text-muted-foreground={!currentPage.endsWith('/partners')}
						class="w-[55px] overflow-hidden whitespace-nowrap hover:text-foreground"
						id="Partners"
						onmouseenter={() => {
							scramble('Partners', 'Partners');
						}}
						onmouseleave={() => (document.getElementById('Partners').innerText = 'Partners')}
					>
						Partners
					</a>
					<a
						href="/about"
						class:text-foreground={currentPage.endsWith('/about')}
						class:text-muted-foreground={!currentPage.endsWith('/about')}
						class="w-[39px] overflow-hidden whitespace-nowrap hover:text-foreground"
						id="About"
						onmouseenter={() => {
							scramble('About', 'About');
						}}
						onmouseleave={() => (document.getElementById('About').innerText = 'About')}
					>
						About
					</a>
					<a
						href="https://tum-blockchain.com"
						class="w-[39px] overflow-hidden whitespace-nowrap text-muted-foreground hover:text-foreground"
						id="Club"
						onmouseenter={() => {
							scramble('Club', 'Club');
						}}
						onmouseleave={() => (document.getElementById('Club').innerText = 'Club')}
					>
						Club
					</a>
				</div>

				<div class="flex h-8 items-center md:gap-4">
					<Button href="mailto:industry@tum-blockchain.com" class="flex h-8 text-sm"
						>Contact Us</Button
					>
					<Button
						variant="invisible"
						class="flex items-center justify-center md:hidden"
						onclick={() => {
							menuOpen = !menuOpen;
						}}
					>
						{#if menuOpen}
							<X class="h-8 w-8 text-zinc-50" />
						{:else}
							<Menu class="h-w h-8 text-zinc-50" />
						{/if}
					</Button>
				</div>
			</div>
		</div>

		{#if menuOpen}
			<div class="mt-10 flex w-full flex-col gap-4">
				<Button
					onclick={() => {
						goto('/projects');
						menuOpen = false;
					}}
					class="w-fit text-base"
					variant="link">PROJECTS</Button
				>
				<Button
					onclick={() => {
						goto('/applicants');
						menuOpen = false;
					}}
					class="w-fit text-base"
					variant="link">APPLICANTS</Button
				>
				<Button
					onclick={() => {
						goto('/partners');
						menuOpen = false;
					}}
					class="w-fit text-base"
					variant="link">PARTNERS</Button
				>
				<Button
					onclick={() => {
						goto('/about');
						menuOpen = false;
					}}
					class="w-fit text-base"
					variant="link">ABOUT</Button
				>
				<Button href="https://tum-blockchain.com" class="w-fit text-base" variant="link"
					>CLUB</Button
				>
			</div>
		{/if}
	</nav>
</header>
