<script>
	import '../app.css';
	import Navbar from '$lib/components/navbar.svelte';
	import Footer from '$lib/components/footer.svelte';
	let { children } = $props();
</script>

<Navbar />

<main class="w-full pt-40">
	{@render children()}
</main>

<Footer />
