<script lang="ts">
	// Components
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import Hero from "$lib/components/layout/hero-sections/Hero.svelte";
</script>

<Hero
	title="Stop scrolling through endless job posts"
	subtitle="Get high-quality design roles matched to your skills with intelligent compatibility scoring. No more wasted hours on irrelevant opportunities."
	imageSrc="/generated/image-a-senior-designer-working-confidently-in.webp"
	centered={false}
	callsToAction={[
		{
			href: "/get-started",
			label: "Find my matches"
		},
		{
			href: "/how-it-works",
			label: "How it works"
		}
	]}
/>
<LogoScroller
	label="Trusted by industry leaders"
	logoUrls={[
		'https://cdn.brandfetch.io/stripe.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/notion.so/w/400/h/400/logo',
		'https://cdn.brandfetch.io/figma.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/linear.app/w/400/h/400/logo'
	]}
/>

<Summary
	title="Smart matching for design careers"
	text="Grids filters thousands of design opportunities through intelligent compatibility scoring, delivering high-quality job matches tailored specifically to senior designers and design managers. Our AI-powered platform eliminates the noise of irrelevant job posts, saving you 15+ hours weekly while connecting you with roles at high-growth tech companies where you'll actually fit."
/>

<Testimonials
	testimonials={[
		{
			name: "Maya Chen",
			position: "Senior Design Manager",
			company: "Stripe",
			quote:
				"Grids saved me 12 hours every week that I was wasting on LinkedIn and job boards. The compatibility scores are incredibly accurate – I landed my dream role at a Series C startup with a 94% team fit match.",
			image: "/generated/image-portrait-of-a-confident-asian-woman-desi.webp"
		},
		{
			name: "Marcus Thompson",
			position: "Lead Product Designer",
			company: "Notion",
			quote:
				"After months of generic job descriptions and mismatched opportunities, Grids connected me with three high-quality roles in just two weeks. The intelligent filtering eliminated all the noise – no more portfolio fatigue.",
			image: "/generated/image-portrait-of-a-thoughtful-black-man-senio.webp"
		},
		{
			name: "Sofia Rodriguez",
			position: "Design Director",
			company: "Linear",
			quote:
				"The team fit percentages changed everything for me. Instead of applying blindly, I could see exactly which companies matched my design philosophy. Reduced my job search time by 65% while finding better opportunities.",
			image: "/generated/image-portrait-of-a-smiling-latina-woman-desig.webp"
		}
	]}
/>

<Features
	title="Intelligent job matching for design professionals"
	subtitle="Stop wasting hours on irrelevant opportunities and discover roles where you'll actually thrive"
	features={[
		{
			title: "AI-powered compatibility scoring",
			description: "Our proprietary algorithms analyze thousands of job parameters against your skills, experience, and preferences to deliver personalized match scores that eliminate guesswork from your career decisions."
		},
		{
			title: "Team fit percentages",
			description: "See exactly how well you'll mesh with potential teams through detailed compatibility breakdowns. Never wonder if you're the right cultural fit again."
		},
		{
			title: "Quality-first filtering",
			description: "We curate opportunities from Series B+ startups and high-growth tech companies, ensuring every role meets our standards for compensation, growth potential, and team quality."
		},
		{
			title: "15+ hours saved weekly",
			description: "Skip the endless scrolling through generic job boards and focus on meaningful opportunities. Our intelligent matching delivers only relevant roles to your personalized dashboard."
		},
		{
			title: "Portfolio optimization insights",
			description: "Combat portfolio fatigue with data-driven recommendations on how to present your work for maximum impact with specific companies and design teams."
		},
		{
			title: "Design community integration",
			description: "Connect directly with hiring managers and design leaders through our network of Series B+ startup communities and exclusive Slack channels."
		}
	]}
/>
<AboutTeaser />
<CallToAction
	title="Ready to stop browsing and start matching?"
	subtitle="Skip the scroll. Land roles that fit."
	description="Join hundreds of senior designers using Grids to cut through the noise and find roles worth applying to. Matches updated weekly, tailored to your skills and goals."
	imageSrc="/generated/image-a-cheerful-and-successful-designer-seate.webp"
	callsToAction={[
		{
			href: "/get-started",
			label: "Try Grids free",
			variant: "primary"
		},
		{
			href: "/how-it-works",
			label: "See how it works",
			variant: "secondary"
		}
	]}
/>
