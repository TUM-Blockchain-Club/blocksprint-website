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
	import stablelab from '$lib/img/stablelab.svg';
	import munichre from '$lib/img/munichre.svg';
	import boersestuttgart from '$lib/img/boersestuttgart.svg';
	import stakingfacilities from '$lib/img/stakingfacilities.svg';
	import hauck from '$lib/img/hauck.svg';
	import rolandberger from '$lib/img/rolandberger.svg';
	import pwc from '$lib/img/pwc.svg';
	import bitvavo from '$lib/img/bitvavo.svg';
</script>

<div
	class="mx-auto flex w-fit max-w-6xl flex-col gap-5 px-3 pt-10 sm:px-6"
	in:blur={{ delay: 50, duration: 300 }}
>
	<h2
		class="text-left text-2xl font-semibold text-foreground sm:text-center sm:text-3xl md:text-4xl"
	>
		BlockSprint Projects
	</h2>
	<p
		class="text max-w-md text-left text-sm text-muted-foreground sm:max-w-3xl sm:text-center sm:text-base md:text-lg"
	>
		BlockSprint connects students with industry partners to solve real-world blockchain challenges.
		Following three impactful iterations, the 4th iteration is coming up, driving innovation and
		bridging academia with the blockchain industry.
	</p>
</div>

<div
	class="mx-auto my-24 flex max-w-6xl flex-col px-3 sm:my-48 sm:px-6"
	in:blur={{ delay: 50, duration: 500 }}
>
	<h2 class="mb-1 text-center text-lg font-medium sm:text-xl md:text-2xl">Fall 2025</h2>
	<p class="mx-auto mb-10 max-w-2xl text-center text-sm text-muted-foreground md:text-base">
		Upcoming
	</p>
	<div class="grid grid-cols-1 gap-[1px] bg-zinc-900 sm:grid-cols-2">
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<div class="-m-0.5">
					<img src={hauck} alt="HADC" class="h-8" />
				</div>
			</div>
			<h2 class="pt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Framework for Smart Contract Lifecycle Management
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Developing a framework for smart contract lifecycle management for tokenization projects.
			</p>
			<Button
				href="https://tum-blockchain-dev.notion.site/HADC-Framework-for-Smart-Contract-Lifecycle-Management-in-Tokenization-Projects-25d486d1154d80a9be88e1a489d5eed7?source=copy_link"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<img src={pwc} alt="PWC" class="h-6" />
			</div>
			<h2 class="mt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Enterprise Blockchain Research Project
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Explore how blockchain, Web3, and AI can help companies during market crises by identifying
				use cases and bridging traditional business with emerging tech.
			</p>
			<Button
				href="https://tum-blockchain-dev.notion.site/PWC-Enterprise-Blockchain-Research-Project-268486d1154d80edb196f06cfcb79ace?source=copy_link"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<div class="flex h-6 items-center">
					<img src={bitvavo} alt="Bitvavo" class="my-auto h-3" />
				</div>
			</div>
			<h2 class="mt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Comparison Landing Page for Exchange & Broker Fees
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Develop a transparent and user-friendly comparison landing page to showcase real-time prices
				and trading fees across crypto exchanges.
			</p>
			<Button
				href="https://tum-blockchain-dev.notion.site/Bitvavo-Market-Analysis-Website-development-263486d1154d8107a2caebecc70508af?source=copy_link"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<img src={rolandberger} alt="Roland Berger" class="h-6" />
			</div>
			<h2 class="mt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Digital Currencies Research Projects
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Explore how banks can design and integrate wallets with additional value-added services and
				identify smart implementation models for the future of banking.
			</p>
			<Button
				href="https://tum-blockchain-dev.notion.site/Roland-Berger-Digital-Currencies-Research-Projects-261486d1154d800caa71d5629f8fd489?source=copy_link"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<img src={stakingfacilities} alt="Staking Facilities" class="h-6" />
			</div>
			<h2 class="mt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Streaming Consensus Data in Sui Network
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Prototype real-time consensus data streaming to improve latency and responsiveness in the
				Sui blockchain.
			</p>
			<Button
				href="https://tum-blockchain-dev.notion.site/Staking-Facilities-Streaming-Consensus-Data-in-Sui-Network-268486d1154d807c8a21e89db08a2f34?source=copy_link"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<p>BMW & Tezos</p>
			</div>
			<h2 class="text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				BMW - Tezos (ENVITED-X to Etherlink)
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Migrate ENVITED-X to Etherlink to enable secure, scalable automotive data sharing.
			</p>
			<Button
				href="https://tum-blockchain-dev.notion.site/BMW-Tezos-Secure-Automotive-Data-Sharing-257486d1154d815cb023ebd26e7a8c08?source=copy_link"
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
	<h2 class="mb-1 text-center text-lg font-medium sm:text-xl md:text-2xl">Spring 2025</h2>
	<p class="mx-auto mb-10 max-w-2xl text-center text-sm text-muted-foreground md:text-base">
		Completed
	</p>
	<div class="grid grid-cols-1 gap-[1px] bg-zinc-900 sm:grid-cols-2">
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<div class="flex h-6 items-center">
					<img src={stablelab} alt="StableLab" class="my-auto h-3" />
				</div>
			</div>
			<h2 class="pt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				AI-Driven DAO Governance
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Expanding decentralized governance solutions with cutting-edge AI.
				<br /><br />
				The project team developed AI solutions to enhance the offering of StableLab and actively contributed
				to the future of DAO governance.
			</p>
			<Button
				href="https://tum-blockchain.notion.site/StableLab-AI-driven-DAO-governance-1a3c28b1e10e80f3b70dd7584b1d3274?pvs=4"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<img src={solanabeach} alt="Solana Beach" class="h-6" />
			</div>
			<h2 class="mt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Mobile App Development
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Building mobile app for monitoring blockchain network activity.
				<br /><br />
				Ambitious students built a user-friendly mobile blockchain explorer, provided real-time insights
				into Solana activity, and enhanced community engagement.
			</p>
			<Button
				href="https://tum-blockchain.notion.site/Solana-Beach-Mobile-App-Development-188fbd739dd443ffb5ab22bfe19ac8e7?pvs=4"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<img src={munichre} alt="Munich Re" class="h-6" />
			</div>
			<h2 class="mt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Crypto AI Agents Security
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Analyzing the existing crypto agent frameworks, pick top performers and implement on
				testnet.
				<br /><br />
				A dedicated team analyzed and deployed Crypto Agents, contributing to AI-driven blockchain security
				and automation.
			</p>
			<Button
				href="https://tum-blockchain.notion.site/Munich-Re-Crypto-AI-Agents-Security-41d28b348f5944ee857ac59734d018b9?pvs=4"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<img src={boersestuttgart} alt="Börse Stuttgart Digital" class="h-6" />
			</div>
			<h2 class="mt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Automated Asset Monitoring
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				A software monitoring system for cryptocurrencies.
				<br /><br />
				The team developed an automated system to improve monitoring, compliance, and risk detection
				for cryptocurrency listings, ensuring regulatory compliance and optimizing resource efficiency.
			</p>
			<Button
				href="https://tum-blockchain.notion.site/B-rse-Stuttgart-Automated-Asset-Monitoring-d68f776c002a4655baad28e25bbdf79a?pvs=4"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<img src={stakingfacilities} alt="Staking Facilities" class="h-6" />
			</div>
			<h2 class="mt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Blockchain Testing Infrastructure
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Setting up and optimizing blockchain testing infrastructure.
				<br /><br />
				The team designed and deployed blockchain testing infrastructure in a Munich data center, focusing
				on hardware configuration, network optimization, and blockchain environment testing.
			</p>
			<Button
				href="https://tum-blockchain.notion.site/Staking-Facilities-Blockchain-Testing-Infrastructure-7a740641cab9472fa9f1ee2c24ea8e1b?pvs=4"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<div class="-m-0.5">
					<img src={hauck} alt="Hauck Aufhäuser" class="h-8" />
				</div>
			</div>
			<h2 class="text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Institutional Wallet Connectivity
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Developing a secure WalletConnect integration for institutional custody.
				<br /><br />
				A pioneering team analyzed and prototyped WalletConnect integration for institutional wallets,
				enhancing security and compliance in regulated crypto custody.
			</p>
			<Button
				href="https://tum-blockchain.notion.site/Hauck-Aufh-user-Digital-Custody-WalletConnect-for-Institutions-1a8c28b1e10e802eb84de5e9ca41b658"
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
	<h2 class="mb-1 text-center text-lg font-medium sm:text-xl md:text-2xl">Fall 2024</h2>
	<p class="mx-auto mb-10 max-w-2xl text-center text-sm text-muted-foreground md:text-base">
		Completed
	</p>
	<div class="grid grid-cols-1 gap-[1px] bg-zinc-900 sm:grid-cols-2">
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<img src={bosch} alt="Bosch" class="h-6" />
			</div>
			<h2 class="pt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Decentralized Marketplace
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Building a decentralized marketplace framework for engineering artifacts.
				<br /><br />
				The team helped Bosch to overcome the limitations in data acquisition and model access during
				the verification and validation stage, where hardware and software were tested in simulation.
			</p>
			<Button
				href="https://tum-blockchain.notion.site/Bosch-Decentralized-Marketplace-for-Automotive-Testing-60c0aab136e544959f67a023c9af5f9e"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<img src={wmdatenservice} alt="WM Datenservice" class="h-6" />
			</div>
			<h2 class="mt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				DeFi Market Research
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				As crypto and digital assets continue to rise, WM Datenservice sees a transformative
				opportunity.
				<br /><br />
				A dedicated team of ambitious students delved deep into the world of crypto data, identifying
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
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<img src={superteamgermany} alt="Superteam Germany" class="h-6" />
			</div>
			<h2 class="mt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Web3 Community Building
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Do you excel at organizing events and have a talent for creating and contributing to
				communities?
				<br /><br />
				The team worked alongside contributors from Superteam Germany and helped grow the Web3 Solana
				community locally and globally.
			</p>
			<Button
				href="https://tum-blockchain.notion.site/Superteam-Project-296f911e23f54e099aa91490f1be8935"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<img src={solanabeach} alt="Solana Beach" class="h-6" />
			</div>
			<h2 class="mt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Fast Stake Shift
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Currently in Solana, shifting stakes between validators is too time-consuming.
				<br /><br />
				The project team developed a layer on top of Solana's native staking, enabling users to seamlessly
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
	<p class="mx-auto mb-10 max-w-2xl text-center text-sm text-muted-foreground md:text-base">
		Completed
	</p>
	<div class="grid grid-cols-1 gap-[1px] bg-zinc-900 sm:grid-cols-2">
		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<img src={deloitte} alt="Deloitte" class="h-6" />
			</div>
			<h2 class="pt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Digital Product Passport
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Europe's Digital Product Passport (DPP) aims to improve the sustainability of products such
				as EV batteries and will be mandatory starting in 2027.
				<br /><br />
				The project team explored opportunities to implement the DPP with blockchain technology and successfully
				implemented it on a blockchain with privacy in mind.
			</p>
			<Button
				href="https://drive.google.com/file/d/1b_TMZREmEgL7LebQyJG_g2nz-G8G-6ZU/view"
				target="_blank"
				rel="noopener"
				class="w-fit text-sm"
				variant="secondary">Learn More</Button
			>
		</div>

		<div class="items-left flex flex-col gap-5 bg-zinc-950 px-3 py-10 sm:p-10">
			<div class="flex w-fit">
				<img src={solanabeach} alt="Solana Beach" class="h-6" />
			</div>
			<h2 class="mt-2 text-xl font-semibold text-foreground sm:text-2xl md:text-3xl">
				Client Research
			</h2>
			<p class="text max-w-md text-sm text-muted-foreground sm:text-base md:text-lg">
				Solana Beach is a platform for exploring the Solana blockchain, offering insights into
				statistics, validators, token metrics, and news about the ecosystem.
				<br /><br />
				The team dived deep into the code of the Solana Labs Client, extracted and categorized relevant
				parameters, and evaluated optimization potential by finetuning parameters.
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
