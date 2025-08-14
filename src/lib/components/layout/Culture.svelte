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
	const { 
		values = [],
		title = "Our culture.",
		subtitle = "The values that guide everything we do",
		imageSrc = "",
		...rest 
	}: { 
		values: Value[]; 
		title?: string;
		subtitle?: string;
		imageSrc?: string;
		[key: string]: any 
	} = $props();

	let cards: HTMLElement[] = $state([]);

	onMount(() => {
		if (!cards.length) return;
		if (window.self !== window.top) return;

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

<section class="bg-white dark:bg-gray-950" {...rest}>
	<div
		class="section-py section-px container mx-auto grid gap-8 [--gap:--spacing(8)] [--radius:var(--radius-2xl)]"
	>
		<SectionHeader {title} {subtitle} />

		{#if imageSrc}
			<div class="grid gap-8 lg:grid-cols-[1fr_2fr] lg:items-center">
				<img
					src={imageSrc}
					alt="Team collaboration"
					class="aspect-[16/9] w-full rounded-lg object-cover"
				/>
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
									<div class="text-headline mb-4">{value.title}</div>
									<div class="text-body text-gray-500 dark:text-gray-400">{value.description}</div>
								</div>
							</div>
						</div>
					{/each}
				</div>
			</div>
		{:else}
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
								<div class="text-headline mb-4">{value.title}</div>
								<div class="text-body text-gray-500 dark:text-gray-400">{value.description}</div>
							</div>
						</div>
					</div>
				{/each}
			</div>
		{/if}
	</div>
</section>
