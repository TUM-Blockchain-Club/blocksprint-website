<script>
	import * as Accordion from '$lib/components/ui/accordion';
	let { category = 'partners' } = $props();
</script>

<div class="mx-auto mt-48 flex max-w-6xl flex-col px-3 sm:px-6">
	<h2 class="mb-4 text-center text-base font-medium sm:text-lg md:text-xl">
		Frequently Asked Questions
	</h2>

	<Accordion.Root>
		<Accordion.Item value="item-1">
			<Accordion.Trigger>
				<p class="text-left text-base">What is BlockSprint?</p>
			</Accordion.Trigger>
			<Accordion.Content>
				<p class="text-sm">
					BlockSprint connects ambitious students with companies to solve Web3-related problems. It
					offers a platform for education, support, and networking within the Web3 ecosystem.
				</p>
			</Accordion.Content>
		</Accordion.Item>
		{#if category === 'partners'}
			<Accordion.Item value="item-2">
				<Accordion.Trigger>
					<p class="text-left text-base">How can our company benefit from participating?</p>
				</Accordion.Trigger>
				<Accordion.Content>
					<p class="text-sm">
						Participating companies gain access to innovative solutions for their Web3 challenges,
						engage with highly qualified talent, and can enhance their employer branding within the
						Web3 community.
					</p>
				</Accordion.Content>
			</Accordion.Item>
		{/if}
		{#if category === 'partners'}
			<Accordion.Item value="item-3">
				<Accordion.Trigger>
					<p class="text-left text-base">What types of projects are suitable for the initiative?</p>
				</Accordion.Trigger>
				<Accordion.Content>
					<p class="text-sm">
						Projects can range from conducting research and developing prototypes to improving
						existing products and processes, as long as they are related to Web3. Our team can help
						refine and structure a project idea to ensure success. Just reach out!
					</p>
				</Accordion.Content>
			</Accordion.Item>
		{/if}
		{#if category === 'students'}
			<Accordion.Item value="item-4">
				<Accordion.Trigger>
					<p class="text-left text-base">How are student participants selected for a project?</p>
				</Accordion.Trigger>
				<Accordion.Content>
					<p class="text-sm">
						The TUM Blockchain Club advertises projects to a large pool of talented students and
						selects a multidisciplinary team to work exclusively on your company's project.
					</p>
				</Accordion.Content>
			</Accordion.Item>
		{/if}
		{#if category === 'partners'}
			<Accordion.Item value="item-5">
				<Accordion.Trigger>
					<p class="text-left text-base">What are the partner requirements?</p>
				</Accordion.Trigger>
				<Accordion.Content>
					<p class="text-sm">
						Partners are expected to provide a clear problem statement or project idea, pitch their
						challenge to students, offer support through a (technical) contact, and establish legal
						agreements for the participants.
					</p>
				</Accordion.Content>
			</Accordion.Item>
		{/if}
		<Accordion.Item value="item-6">
			<Accordion.Trigger>
				<p class="text-left text-base">What is the project timeline and structure?</p>
			</Accordion.Trigger>
			<Accordion.Content>
				<p class="text-sm">
					The upcoming program runs from October 18th to January 10th, during which participants are
					organized into teams of 3-4. During these 12 weeks, there will be with milestones
					including a kick-off event, mid-term presentation, and final presentation. Moreover, a
					dedicated project mentor from TBC will support the team with weekly calls and guidance,
					ensuring a structured approach to achieving project goals.
				</p>
			</Accordion.Content>
		</Accordion.Item>
		{#if category === 'partners'}
			<Accordion.Item value="item-7">
				<Accordion.Trigger>
					<p class="text-left text-base">What does the financial commitment look like?</p>
				</Accordion.Trigger>
				<Accordion.Content>
					<p class="text-sm">
						Organizations sponsor the project with a budget that covers student compensation, event
						organization, marketing, HR, and project support, with detailed cost structures provided
						based on the team size.
					</p>
				</Accordion.Content>
			</Accordion.Item>
		{/if}
		<Accordion.Item value="item-8">
			<Accordion.Trigger>
				<p class="text-left text-base">How can I reach out to the TBC?</p>
			</Accordion.Trigger>
			<Accordion.Content>
				<p class="text-sm">
					To reach out to us, you can either fill out the contact form on our website to leave your
					email, and we will get back to you promptly. Alternatively, you can directly email us at
					<a href="mailto:industry@tum-blockchain.com" class="hover:underline"
						>industry@tum-blockchain.com</a
					> for any inquiries or further information regarding partnerships and projects.
				</p>
			</Accordion.Content>
		</Accordion.Item>
	</Accordion.Root>
</div>
