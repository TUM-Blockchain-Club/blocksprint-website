<script>
	const milestones = [
		{
			date: '11/2023',
			title: 'Formation of the Industry Team'
		},
		{
			date: '04/2024',
			title: 'Kick-off Event for the first Iteration'
		},
		{
			date: '05/2024',
			title: 'Midterm Checkpoint for the first Iteration'
		},
		{
			date: '07/2024',
			title: 'Final Event of the first Iteration'
		},
		{
			date: '10/2024',
			title: 'Kick-off Event for the second Iteration'
		}
	];
</script>

<section class="w-full px-4 py-16 md:px-6 lg:px-8">
	<div class="mx-auto max-w-6xl">
		<h2 class="mb-8 text-center text-lg font-bold sm:mb-12 sm:text-xl md:mb-16 md:text-2xl">
			BlockSprint: Key Milestones & Timeline
		</h2>

		<!-- Desktop Timeline -->
		<div class="relative hidden items-center justify-between md:flex">
			<!-- Connecting Line -->
			<div class="absolute left-0 right-0 top-4 h-[2px] rounded-full bg-zinc-50"></div>

			<!-- Milestones -->
			{#each milestones as milestone, index}
				<div class="relative flex w-48 flex-col items-center">
					<!-- Circle -->
					<div class="relative z-10 h-8 w-8 rounded-full bg-zinc-50"></div>

					<!-- Date -->
					<div class="mt-6 text-lg font-medium">
						{milestone.date}
					</div>

					<!-- Title -->
					<div class="mt-2 text-center text-sm">
						{milestone.title}
					</div>
				</div>
			{/each}
		</div>

		<!-- Mobile Timeline -->
		<div class="mx-auto w-fit md:hidden">
			{#each milestones as milestone, index}
				<div class="flex items-start space-x-4">
					<!-- Circle and Vertical Line -->
					<div class="flex flex-col items-center">
						<div class="h-6 w-6 rounded-full bg-zinc-50"></div>
						{#if index !== milestones.length - 1}
							<div class="h-24 w-[2px] rounded-full bg-zinc-50"></div>
						{/if}
					</div>

					<!-- Content -->
					<div class="pt-1">
						<div class="font-medium">
							{milestone.date}
						</div>
						<div class="mt-1 text-sm">
							{milestone.title}
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>
