<script>
	import bosch from '$lib/img/bosch.svg';
	import deloitte from '$lib/img/deloitte.svg';
	import solanabeach from '$lib/img/solanabeach.svg';
	import superteamgermany from '$lib/img/superteamgermany.svg';
	import wmdatenservice from '$lib/img/wmdatenservice.svg';
	import Marquee from 'svelte-fast-marquee';
</script>

<div class="mx-auto mt-32 max-w-6xl px-3 sm:px-6" in:blur={{ delay: 200, duration: 450 }}>
	<h2 class="mb-10 text-center text-base font-medium sm:text-lg md:text-xl">
		Former Project Partners <br /><span class="text-muted-foreground">
			From Startup to Enterprise - we got you.
		</span>
	</h2>
</div>
<div in:blur={{ delay: 200, duration: 500 }}>
	<Marquee gap="70px" speed={30}>
		<img src={bosch} alt="Bosch" class="mx-auto h-8" />
		<img src={wmdatenservice} alt="WM Datenservice" class="mx-auto h-8" />
		<img src={deloitte} alt="Deloitte" class="mx-auto h-8" />
		<img src={solanabeach} alt="Solanabeach" class="mx-auto h-8" />
		<img src={superteamgermany} alt="Superteam Germany" class="mx-auto h-8" />
	</Marquee>
</div>
