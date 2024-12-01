<script>
	import { Button } from '$lib/components/ui/button/index.js';
	import { scramble } from '$lib/utils/scramble.js';
	import tbc from '$lib/img/tbc.svg';
	import { Menu, X } from 'lucide-svelte';
	import { goto } from '$app/navigation';

	let menuOpen = $state(false);

	$effect(() => {
		document.body.style.overflow = menuOpen ? 'hidden' : '';
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

			<div class="hidden items-center gap-4 text-sm md:flex lg:gap-8">
				<a
					href="/projects"
					class="w-[71px] overflow-hidden whitespace-nowrap text-muted-foreground hover:text-foreground"
					id="projects"
					onmouseenter={() => {
						scramble('projects', 'PROJECTS');
					}}
					onmouseleave={() => (document.getElementById('projects').innerText = 'PROJECTS')}
				>
					PROJECTS
				</a>
				<a
					href="/applicants"
					class="w-[83px] overflow-hidden whitespace-nowrap text-muted-foreground hover:text-foreground"
					id="applicants"
					onmouseenter={() => {
						scramble('applicants', 'APPLICANTS');
					}}
					onmouseleave={() => (document.getElementById('applicants').innerText = 'APPLICANTS')}
				>
					APPLICANTS
				</a>
				<a
					href="/partners"
					class="w-[71px] overflow-hidden whitespace-nowrap text-muted-foreground hover:text-foreground"
					id="partners"
					onmouseenter={() => {
						scramble('partners', 'PARTNERS');
					}}
					onmouseleave={() => (document.getElementById('partners').innerText = 'PARTNERS')}
				>
					PARTNERS
				</a>
				<a
					href="/about"
					class="w-[47px] overflow-hidden whitespace-nowrap text-muted-foreground hover:text-foreground"
					id="about"
					onmouseenter={() => {
						scramble('about', 'ABOUT');
					}}
					onmouseleave={() => (document.getElementById('about').innerText = 'ABOUT')}
				>
					ABOUT
				</a>
			</div>

			<div class="flex h-8 items-center md:gap-4">
				<Button class="flex h-8 text-sm">Partnership</Button>
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

		{#if menuOpen}
			<div class="mt-10 flex w-full flex-col gap-4">
				<Button
					onclick={() => {
						menuOpen = false;
						goto('/projects');
					}}
					class="w-fit text-base"
					variant="link">PROJECTS</Button
				>
				<Button
					onclick={() => {
						menuOpen = false;
						goto('/applicants');
					}}
					class="w-fit text-base"
					variant="link">APPLICANTS</Button
				>
				<Button
					onclick={() => {
						menuOpen = false;
						goto('/partners');
					}}
					class="w-fit text-base"
					variant="link">PARTNERS</Button
				>
				<Button
					onclick={() => {
						menuOpen = false;
						goto('/about');
					}}
					class="w-fit text-base"
					variant="link">ABOUT</Button
				>
			</div>
		{/if}
	</nav>
</header>
