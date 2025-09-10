<script>
	import { Calendar, Rocket } from '@lucide/svelte';

	let { tag, title, subtitle, milestones = [] } = $props();
</script>

<section class="w-full">
	<div class="mx-auto grid max-w-6xl grid-cols-1 gap-20 px-3 sm:px-6 md:grid-cols-2 md:gap-0">
		<div class="mx-auto flex h-fit flex-col md:sticky md:top-32 md:mx-0">
			<div class="mx-auto flex items-center gap-2.5 font-medium text-[#CD31FF] md:mx-0">
				<Rocket class="h-4 w-4" />
				<p>{tag}</p>
			</div>
			<h2 class="font-display mt-8 text-balance text-center text-3xl font-medium md:text-left">
				{title}
			</h2>
			<p class="mt-3 max-w-md text-pretty text-center text-lg text-muted-foreground md:text-left">
				{subtitle}
			</p>
		</div>

		<div class="mx-auto w-fit md:mx-0">
			{#each milestones as milestone, index}
				<div class="flex items-start space-x-4">
					<!-- Circle and Vertical Line -->
					<div class="flex flex-col items-center">
						<div
							class="flex h-12 w-12 items-center justify-center rounded-full border border-zinc-800 bg-zinc-950"
						>
							<Calendar class="h-5 w-5 text-foreground" />
						</div>
						{#if index !== milestones.length - 1}
							<div class="h-24 w-[1px] rounded-full bg-zinc-800"></div>
						{/if}
					</div>

					<!-- Content -->
					<div>
						<div class="font-medium text-foreground">
							{milestone.title}
						</div>
						<div class="mt-1 text-sm text-muted-foreground">
							{milestone.date}
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>
