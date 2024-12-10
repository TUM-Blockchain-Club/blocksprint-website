<script>
	import bosch from '$lib/img/bosch.svg';
	import deloitte from '$lib/img/deloitte.svg';
	import solanabeach from '$lib/img/solanabeach.svg';
	import superteamgermany from '$lib/img/superteamgermany.svg';
	import wmdatenservice from '$lib/img/wmdatenservice.svg';
	import Marquee from 'svelte-fast-marquee';
</script>

<div class="mx-auto mt-32 max-w-6xl px-3 sm:px-6">
	<h2 class="mb-1 text-center text-lg font-medium sm:text-xl md:text-2xl">Project Partners</h2>
	<p class="mx-auto mb-10 max-w-md text-center text-sm text-muted-foreground md:text-base">
		We connect partners with the best student talent for their Web3-related projects.
	</p>
</div>
<div class="relative mx-auto max-w-6xl">
	<div
		class="pointer-events-none absolute left-0 z-10 h-full w-16 bg-gradient-to-r from-background to-transparent sm:w-32 md:w-64"
	></div>
	<div
		class="pointer-events-none absolute right-0 z-10 h-full w-16 bg-gradient-to-l from-background to-transparent sm:w-32 md:w-64"
	></div>

	<Marquee gap="70px" speed={30}>
		<img src={bosch} alt="Bosch" class="mx-auto h-8" />
		<img src={wmdatenservice} alt="WM Datenservice" class="mx-auto h-8" />
		<img src={deloitte} alt="Deloitte" class="mx-auto h-8" />
		<img src={solanabeach} alt="Solanabeach" class="mx-auto h-8" />
		<img src={superteamgermany} alt="Superteam Germany" class="mx-auto h-8" />
	</Marquee>
</div>
