<script lang="ts">
	import '../app.css';
	import { GeistSans } from 'geist-svelte/font/sans';
	import { GeistMono } from 'geist-svelte/font/mono';
	import Navbar from '$lib/components/navbar.svelte';
	import Footer from '$lib/components/footer.svelte';
	let { children } = $props();
</script>

<Navbar />

<main class="w-full pt-40">
	{@render children()}
</main>

<Footer />
