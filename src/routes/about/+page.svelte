<script>
	import Footer from '$lib/components/footer.svelte';
	import Timeline from '$lib/components/timeline.svelte';
	import { ChevronRight, Key, Telescope, Linkedin } from 'lucide-svelte';
	import { Button } from '$lib/components/ui/button/index.js';
	import { blur } from 'svelte/transition';
	import giga from '$lib/img/gigachad.jpeg';
	import daniel from '$lib/img/daniel.jpg';
	import aysenur from '$lib/img/aysenur.jpg';
	import ekaterina from '$lib/img/ekaterina.png';
	import daniil from '$lib/img/daniil.jpg';
	import tian from '$lib/img/tian.jpg';
	import ji from '$lib/img/ji.jpeg';
	import felix from '$lib/img/felix.png';
	import thomas from '$lib/img/thomas.png';
	import hofmann from '$lib/img/hofmann.jpg';
	import georg from '$lib/img/georg.jpg';
	import laura from '$lib/img/laura.jpg';
	import anoushk from '$lib/img/anoushk.jpg';

	let milestones = [
		{
			date: '11/2023',
			title: 'Formation of the Industry Team'
		},
		{
			date: '04/2024 - 07/2024',
			title: 'First Iteration of the BlockSprint'
		},
		{
			date: '10/2024 - 01/2025',
			title: 'Second Iteration of the BlockSprint'
		},
		{
			date: '05/2025 - 08/2025',
			title: 'Third Iteration of the BlockSprint'
		}
	];

	let members = [
		{
			image: georg,
			name: 'Georg Beyschlag',
			linkedin: 'https://www.linkedin.com/in/georg-beyschlag-46bab0177'
		},
		{
			image: laura,
			name: 'Laura Gullicksen',
			linkedin: 'https://www.linkedin.com/in/laura-g-51262a1a1/'
		},
		{
			image: hofmann,
			name: 'Jakob Hofmann',
			linkedin: 'https://www.linkedin.com/in/jakob-hofmann-b413aa240/'
		},
		{
			image: ji,
			name: 'Jakob Isermann',
			linkedin: 'https://www.linkedin.com/in/jis3r/'
		},
		{
			image: anoushk,
			name: 'Anoushk Kolagotla',
			linkedin: 'https://www.linkedin.com/in/anoushkv/'
		},
		{
			image: daniil,
			name: 'Daniil Korenkov',
			linkedin: 'https://www.linkedin.com/in/daniil-korenkov-937523252'
		},
		{
			image: ekaterina,
			name: 'Ekaterini Laro',
			linkedin: 'https://www.linkedin.com/in/katerina-laro-992335198/'
		},
		{
			image: aysenur,
			name: 'Ayşenur Özbek',
			linkedin: 'https://www.linkedin.com/in/ayşenur-özbek-29b801109'
		},
		{
			image: felix,
			name: 'Felix Rihacek',
			linkedin: 'https://www.linkedin.com/in/felix-rihacek/'
		},
		{
			image: tian,
			name: 'Tian Tang',
			linkedin: 'https://www.linkedin.com/in/tian-tang-0384aa2a8/'
		},
		{
			image: thomas,
			name: 'Thomas Wagner',
			linkedin: 'https://www.linkedin.com/in/thomas-wagner97/'
		},
		{
			image: daniel,
			name: 'Daniel Wiedenmann',
			linkedin: 'https://www.linkedin.com/in/daniel-wiedenmann/'
		}
	];
</script>

<div
	class="mx-auto grid max-w-6xl gap-10 px-3 pb-32 sm:grid-cols-2 sm:px-6 sm:pt-10"
	in:blur={{ delay: 50, duration: 300 }}
>
	<div class="order-2 flex items-center justify-center sm:order-1">
		<Telescope
			class="mx-auto h-56 w-56 text-zinc-800 sm:h-64 sm:w-64 md:h-72 md:w-72"
			strokeWidth=".25"
		/>
	</div>
	<div class="order-1 flex flex-col gap-5 sm:order-2">
		<h2 class="text-2xl font-semibold text-foreground sm:text-3xl md:text-4xl">Our Vision</h2>
		<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
			We bridge the gap between academia and the industry by organizing Industry Projects. Ambitious
			students tackle Web3 challenges and create value for our industry partners.
			<br /><br />
			By fostering collaboration between academia and industry, we are accelerating Web3 innovation and
			empowering a new generation of builders.
		</p>
	</div>
</div>

<div in:blur={{ delay: 50, duration: 400 }}>
	<Timeline {milestones} tag="History" title="BlockSprint" subtitle="Key Milestones & Timeline" />
</div>

<div
	class="mx-auto mt-48 flex max-w-6xl flex-col px-3 sm:px-6"
	in:blur={{ delay: 50, duration: 500 }}
>
	<h2 class="mb-1 text-center text-lg font-medium sm:text-xl md:text-2xl">
		Meet the Industry Team
	</h2>
	<p class="mx-auto mb-10 max-w-2xl text-center text-sm text-muted-foreground md:text-base">
		Passionate members of the TUM Blockchain Club, dedicated to bridging the gap between students
		and groundbreaking companies, driving innovation for the future of the industry.
	</p>
	<div class="grid grid-cols-2 gap-[1px] bg-zinc-900 md:grid-cols-3 lg:grid-cols-4">
		{#each members as member}
			<div class="flex flex-col justify-between bg-zinc-950 p-8 lg:p-10">
				<div class="items-left flex flex-col justify-center">
					<img src={member.image} alt={member.name} class="w-full rounded-lg" />
					<p class="mt-4 text-foreground sm:text-lg md:text-xl">{member.name}</p>
					<a
						href={member.linkedin}
						target="_blank"
						rel="noopener"
						class="mt-1 w-fit text-sm text-muted-foreground transition-colors hover:text-foreground"
					>
						<Linkedin class="h-5 w-5" />
					</a>
				</div>
				<div></div>
			</div>
		{/each}
	</div>
</div>
