<script>
	import { ChevronRight } from '@lucide/svelte';
	import { Button } from '$lib/components/ui/button/index.js';
	import { onMount } from 'svelte';

	let gradientAngle = 0;

	onMount(() => {
		const animateGradient = () => {
			gradientAngle = (gradientAngle + 1) % 360;
			requestAnimationFrame(animateGradient);
		};

		const animation = requestAnimationFrame(animateGradient);

		return () => {
			cancelAnimationFrame(animation);
		};
	});
</script>

<div
	class="border-gradient w-fit overflow-hidden rounded-md transition-transform duration-300"
	style:--gradient-angle="{gradientAngle}deg"
>
	<Button
		href="https://apply.tum-blockchain.com/talent-pool"
		variant="ghost"
		class="relative z-10 flex gap-1 hover:bg-zinc-900"
	>
		<p class="bg-gradient-to-r from-zinc-50 to-zinc-400 bg-clip-text text-transparent">
			Join our Talent Pool
		</p>
		<ChevronRight class="h-5 w-5" />
	</Button>
</div>

<style>
	.border-gradient {
		--c: #09090b;
		--p: 10%;
		--gradient-angle: 0deg;
		background:
			linear-gradient(var(--c), var(--c)) padding-box,
			conic-gradient(
					from var(--gradient-angle),
					transparent,
					white var(--p),
					transparent calc(var(--p) * 2)
				)
				border-box;
		border: 1px solid transparent;
		position: relative;
	}
</style>
