<script lang="ts">
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import { animate, stagger } from "motion";
	import { onMount } from "svelte";

	// Types
	export type Value = {
		title: string;
		description: string;
	};

	// Props
	const { values = [
  {
    title: 'Impact you see, not just ship',
    description: 'Every project touches real customer operations—days, not quarters, from code to results.'
  },
  {
    title: 'Small team, big reach',
    description: 'We operate as a tight, high-output group—collaborating daily without layers. Everyone’s voice matters.'
  },
  {
    title: 'Curiosity for how things work',
    description: 'We’re relentless about understanding the details—from ERP workflows to why customers call support.'
  },
  {
    title: 'Pragmatism over perfection',
    description: 'We value outcomes. Solutions are chosen for what gets the job done, not what looks fanciest.'
  },
  {
    title: 'Own your craft, trust your team',
    description: 'Autonomy and trust are nonnegotiable. We expect initiative and transparency from everyone.'
  },
  {
    title: 'Fixing overlooked problems',
    description: 'We’re here for the big, unglamorous challenges dropped by everyone else—the backbone of the economy.'
  }
]: { values: Value[] } = $props();

	let cards: HTMLElement[] = $state([]);

	onMount(() => {
		if (!cards.length) return;
		animate(
			cards,
			{
				y: ["1.5rem", 0],
				filter: ["blur(2px)", "blur(0px)"],
				opacity: [0, 1]
			},
			{
				duration: 0.3,
				ease: "easeOut",
				delay: stagger(0.1, {
					ease: "easeInOut"
				})
			}
		);
	});
</script>

<section class="bg-white dark:bg-gray-950">
	<div
		class="section-py section-px container mx-auto grid gap-8 [--gap:--spacing(8)] [--radius:var(--radius-2xl)]"
	>
		<SectionHeader title="Built for impact, not hype." subtitle="What it means to work at Commerce Systems" />

		<div
			class="grid gap-(--gap)"
			style:grid-template-columns="repeat(auto-fit, minmax(280px, 1fr))"
		>
			{#each values as value, i}
				<div
					bind:this={cards[i]}
					class="relative border-t border-gray-200 pt-4 dark:border-gray-900"
				>
					<!-- Content -->
					<div class="text-caption z-10">
						<div>
							<div class="text-headline mb-[1em]">{value.title}</div>
							<div class="text-body text-gray-500 dark:text-gray-400">{value.description}</div>
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>
