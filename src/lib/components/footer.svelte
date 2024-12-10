<script>
	import fattbc from '$lib/img/fattbc.svg';
	import Button from '$lib/components/ui/button/button.svelte';
	import { onMount } from 'svelte';

	let mounted = false;

	onMount(() => {
		mounted = true;
	});
</script>

{#if mounted}
	<footer class="mx-auto mt-16 max-w-6xl p-3 sm:mt-28 md:mt-40">
		<img src={fattbc} alt="TUM Blockchain Club" class="mb-12 w-full md:mb-16" />
		<div class="flex flex-col justify-between sm:flex-row md:pr-12">
			<div class="order-2 flex flex-col justify-between sm:order-1">
				<div></div>
				<p class="mx-auto mt-4 text-sm text-muted-foreground sm:mx-0 sm:mt-0">
					Copyright © TUM Blockchain Club
				</p>
			</div>
			<div class="smflex order-1 grid grid-cols-2 gap-16 sm:order-2">
				<div class="flex flex-col">
					<p class="mb-8 text-sm text-foreground">Legal</p>
					<a
						href="https://www.tum-blockchain.com/imprint"
						target="_blank"
						rel="noopener"
						class="mb-4 text-sm text-muted-foreground hover:underline">Imprint</a
					>
					<a
						href="https://www.tum-blockchain.com/privacy-policy"
						target="_blank"
						rel="noopener"
						class="mb-4 text-sm text-muted-foreground hover:underline">Privacy</a
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
	</footer>
{/if}
