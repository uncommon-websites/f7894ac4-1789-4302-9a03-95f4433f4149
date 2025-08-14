<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Quality over quantity",
			description: "We believe designers deserve better than endless scrolling through irrelevant opportunities. Every match is carefully filtered through intelligent algorithms to ensure meaningful compatibility."
		},
		{
			title: "Design community first",
			description: "Built by designers, for designers. We understand the creative process, portfolio fatigue, and the unique challenges of finding roles that truly value design excellence."
		},
		{
			title: "Transparent matching",
			description: "No black box algorithms or hidden metrics. Our platform shows you real team fit percentages and concrete compatibility scores, so you can make informed career decisions with confidence."
		}
	];
</script>

<SecondaryHero
	title="Better matches, fewer dead ends"
	subtitle="Cut through the noise in job search"
	imageSrc="/generated/image-a-group-of-diverse-professionals-collabo.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"Every designer knows the frustration. You're scrolling through endless job posts at midnight, wading through vague descriptions and irrelevant opportunities that don't match your skills or values. Senior designers and design managers at high-growth companies waste 15+ hours weekly searching for roles that actually fit, burning creative energy on tedious job discovery instead of doing what they love most—designing.",
		"That's why Didier Catz and Max Potze built Grids. Instead of adding more noise to an already overwhelming market, they created intelligent compatibility scoring algorithms that filter thousands of opportunities down to the ones that actually matter. Our platform shows real team fit percentages and meaningful matches, replacing generic job descriptions with insights that help you make informed decisions about your next career move.",
		"Today, we're transforming how design professionals find their next opportunity in the $15B recruitment technology market. By connecting 100K active matches through design community networks and eliminating portfolio fatigue, we're helping senior designers at Series B+ startups discover quality roles without the endless searching. Because great designers deserve better than scrolling—they deserve matches that make sense."
	]}
/>

<!-- Our Culture Section -->
<Culture 
	{values}
	title="Our values"
	subtitle="What drives us to build better job matching"
	imageSrc="/generated/image-a-diverse-design-team-of-five-members-in.webp"
/>

<!-- StakeholderGrid Section -->
<StakeholderGrid
	stakeholderType="team"
	title="Meet the founders"
	subtitle="Building the future of job matching"
	stakeholders={[
		{
			name: "Max Potze",
			position: "Co-founder & CEO",
			bio: "Passionate about solving the inefficiencies in design talent discovery through intelligent algorithms.",
			image: "/generated/image-a-professional-headshot-of-a-confident-b.webp"
		},
		{
			name: "Didier Catz",
			position: "Co-founder & CTO",
			bio: "Architecting scalable systems that match design professionals with opportunities that truly fit.",
			image: "/generated/image-a-professional-headshot-of-a-business-le.webp"
		}
	]}
/>

<!-- CTA Section -->
<CallToAction
	title="Stop endless job searching"
	subtitle="Start intelligent matching instead"
	description="Join 100K active designers who've discovered quality roles through our compatibility scoring algorithms. See your team fit percentage before you apply, not after weeks of waiting."
	imageSrc="/generated/image-professional-designer-working-in-a-bright.webp"
/>
