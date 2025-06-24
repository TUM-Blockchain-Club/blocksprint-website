<script>
	import fattbc from '$lib/img/fattbc.svg';
	import fatindustry from '$lib/img/fatindustry.svg';
	import Button from '$lib/components/ui/button/button.svelte';
	import { onMount } from 'svelte';

	let mounted = false;

	onMount(() => {
		mounted = true;
	});
</script>

{#if mounted}
	<footer class="border-t border-border">
		<div class="mx-auto max-w-6xl px-3">
			<div class="my-12 flex flex-col justify-between md:my-16">
				<div class="flex w-full justify-between">
					<div></div>

					<div class="grid grid-cols-2 gap-16 sm:flex">
						<div class="flex flex-col">
							<p class="mb-8 text-sm text-foreground">Legal</p>
							<a
								href="https://www.tum-blockchain.com/imprint"
								target="_blank"
								rel="noopener"
								class="mb-4 text-sm text-muted-foreground hover:underline">Imprint</a
							>
							<a
								href="https://drive.google.com/file/d/1TcXdGF5jARyVKreqJ4ht3Q2ICGOEuyPt/view"
  								class="mb-4 text-sm text-muted-foreground hover:underline">
  								Privacy</a
							>
							<a
								href="mailto:industry@tum-blockchain.com"
								class="mb-4 text-sm text-muted-foreground hover:underline">Contact</a
							>
						</div>
						<div class="flex flex-col">
							<p class="mb-8 text-sm text-foreground">Connect</p>
							<a
								href="https://x.com/tbc_munich"
								target="_blank"
								rel="noopener"
								class="mb-4 text-sm text-muted-foreground hover:underline">Twitter</a
							>
							<a
								href="https://www.linkedin.com/company/tum-blockchain-club/"
								target="_blank"
								rel="noopener"
								class="mb-4 text-sm text-muted-foreground hover:underline">LinkedIn</a
							>
							<a
								href="https://www.instagram.com/tumblockchain/"
								target="_blank"
								rel="noopener"
								class="mb-4 text-sm text-muted-foreground hover:underline">Instagram</a
							>
							<a
								href="https://discord.gg/kqwYF2cHb9"
								target="_blank"
								rel="noopener"
								class="mb-4 text-sm text-muted-foreground hover:underline">Discord</a
							>
						</div>
					</div>
				</div>
				<div class="flex w-full justify-between">
					<p class="mx-0 mt-4 text-sm text-muted-foreground sm:mt-0">
						Copyright © TUM Blockchain Club
					</p>
					<div></div>
				</div>
			</div>
			<img src={fatindustry} alt="FAT Industry" class="w-full" />
		</div>
	</footer>
{/if}
