<script>
	import Footer from '$lib/components/footer.svelte';
	import Partners from '$lib/components/partners.svelte';
	import { blur } from 'svelte/transition';
	import {
		ChevronRight,
		Key,
		Telescope,
		Users,
		Award,
		Phone,
		Briefcase,
		Handshake,
		Target,
		Blocks,
		GraduationCap,
		HandCoins,
		PocketKnife,
		Rocket
	} from 'lucide-svelte';
	import { Button } from '$lib/components/ui/button/index.js';
	import bosch from '$lib/img/bosch.svg';
	import deloitte from '$lib/img/deloitte.svg';
	import solanabeach from '$lib/img/solanabeach.svg';
	import superteamgermany from '$lib/img/superteamgermany.svg';
	import wmdatenservice from '$lib/img/wmdatenservice.svg';
</script>

<div
	class="mx-auto flex w-fit max-w-6xl flex-col gap-5 px-3 pt-10 sm:px-6"
	in:blur={{ delay: 50, duration: 300 }}
>
	<h2 class="text-center text-2xl font-semibold text-foreground sm:text-3xl md:text-4xl">
		BlockSprint Projects
	</h2>
	<p class="text max-w-3xl text-center text-sm text-muted-foreground sm:text-base md:text-lg">
		BlockSprint is a hands-on project initiative by the TUM Blockchain Club, where students
		collaborate with industry partners to tackle real-world blockchain challenges. We successfully
		completed the 1st iteration, where student teams worked on innovative solutions for various
		industry projects. Currently, we are in the 2nd iteration, continuing our mission to bridge the
		gap between academia and the blockchain industry through impactful projects.
	</p>
</div>

<div
	class="mx-auto my-24 flex max-w-6xl flex-col px-3 sm:my-48 sm:px-6"
	in:blur={{ delay: 50, duration: 500 }}
>
	<h2 class="mb-1 text-center text-lg font-medium sm:text-xl md:text-2xl">Fall 2024</h2>
	<p
		class="mx-auto mb-10 max-w-2xl text-center text-xs text-muted-foreground sm:text-sm md:text-base"
	>
		Ongoing
	</p>
	<div class="grid grid-cols-1 gap-[1px] bg-zinc-900 sm:grid-cols-2">
		<div class="flex flex-col gap-5 bg-zinc-950 p-4 sm:p-10">
			<img src={bosch} alt="Bosch" class="h-6 w-fit" />
			<h2 class="pt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Decentralized Marketplace
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Building a decentralized marketplace framework for engineering artifacts.
				<br /><br />
				The team helps Bosch to overcome the current limitations in data acquisition and model access
				of the verification and validation stage - where hardware and software are tested in simulation.
			</p>
			<Button
				href="https://tum-blockchain.notion.site/Bosch-Decentralized-Marketplace-for-Automotive-Testing-60c0aab136e544959f67a023c9af5f9e"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
		<div class="flex flex-col gap-5 bg-zinc-950 p-4 sm:p-10">
			<img src={wmdatenservice} alt="WM Datenservice" class="h-6 w-fit" />
			<h2 class="mt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				DeFi Market Research
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				As crypto and digital assets continue to rise, WM Datenservice sees a transformative
				opportunity.
				<br /><br />
				A dedicated team of ambitious students will delve deep into the world of crypto data, identifying
				innovative products or services that could shape the future of finance.
			</p>
			<Button
				href="https://tum-blockchain.notion.site/WM-Datenservice-DeFi-Market-Research-eb9cc8fc6b194f178ab399868a9a2632"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
		<div class="flex flex-col gap-5 bg-zinc-950 p-4 sm:p-10">
			<img src={superteamgermany} alt="Superteam Germany" class="h-6 w-fit" />
			<h2 class="mt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Web3 Community Building
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Do you excel at organizing events and have a talent for creating and contributing to
				communities?
				<br /><br />
				Work alongside contributors from Superteam Germany and help grow the Web3 Solana community locally
				and globally.
			</p>
			<Button
				href="https://tum-blockchain.notion.site/Superteam-Project-296f911e23f54e099aa91490f1be8935"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
		<div class="flex flex-col gap-5 bg-zinc-950 p-4 sm:p-10">
			<img src={solanabeach} alt="Solana Beach" class="h-6 w-fit" />
			<h2 class="mt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Fast Stake Shift
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Currently in Solana, shifting stakes between validators is too time-consuming.
				<br /><br />
				The project team will develop a layer on top of Solana's native staking, enabling users to seamlessly
				shift stakes in just one transaction.
			</p>
			<Button
				href="https://tum-blockchain.notion.site/Solana-Beach-Fast-Stake-Shift-Project-a2c948f1673f41d0830bc94c2f743f17"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
	</div>
</div>

<div
	class="mx-auto my-24 flex max-w-6xl flex-col px-3 sm:my-48 sm:px-6"
	in:blur={{ delay: 50, duration: 500 }}
>
	<h2 class="mb-1 text-center text-lg font-medium sm:text-xl md:text-2xl">Spring 2024</h2>
	<p
		class="mx-auto mb-10 max-w-2xl text-center text-xs text-muted-foreground sm:text-sm md:text-base"
	>
		Completed
	</p>
	<div class="grid grid-cols-1 gap-[1px] bg-zinc-900 sm:grid-cols-2">
		<div class="flex flex-col gap-5 bg-zinc-950 p-4 sm:p-10">
			<img src={deloitte} alt="Deloitte" class="h-6 w-fit" />
			<h2 class="pt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Digital Product Passport
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Europe's Digital Product Passport (DPP) aims to improve the sustainability of products such
				as EV batteries and will be mandatory starting in 2027.
				<br /><br />
				The project team will explore opportunities to implement the DPP with blockchain tech. The project
				goal is to implement the DPP on a blockchain with privacy in mind.
			</p>
			<Button
				href="https://drive.google.com/file/d/1b_TMZREmEgL7LebQyJG_g2nz-G8G-6ZU/view"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>

		<div class="flex flex-col gap-5 bg-zinc-950 p-4 sm:p-10">
			<img src={solanabeach} alt="Solana Beach" class="h-6 w-fit" />
			<h2 class="mt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Client Research
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Solana Beach is a platform for exploring the Solana blockchain, offering insights into
				statistics, validators, token metrics, and news about the ecosystem.
				<br /><br />
				Dive deep into the code of the Solana Labs Client. Extract and categorize relevant parameters.
				Evaluate optimization potential by finetuning parameters.
			</p>
			<Button
				href="https://docs.google.com/presentation/d/1XU-n3fTOR0Pr5ouDvQflQSCauU_MHcriMMExMMc_3VI/edit#slide=id.g2bfb78af382_0_2035"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
	</div>
</div>
