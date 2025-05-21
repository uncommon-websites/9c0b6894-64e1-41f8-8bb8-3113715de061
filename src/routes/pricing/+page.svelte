<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
  testimonials={[
    {
      name: "Vanessa Lim",
      position: "COO",
      company: "Silverpoint Technologies",
      quote: "Commerce cut 80% of support headcount within weeks—and our order turnaround actually got faster.",
      image: "/generated/image-a-professional-headshot-of-vanessa-lim-a.webp"
    },
    {
      name: "Caleb Moreno",
      position: "VP Finance",
      company: "Linden AQ",
      quote: "Your COGS AI gave us clarity we didn’t think was possible without a full FP&A team.",
      image: "/generated/image-a-professional-headshot-of-caleb-moreno-.webp"
    },
    {
      name: "Sarah Greene",
      position: "Dir. of Buying Ops",
      company: "Threadwell Homes",
      quote: "We send chaotic PO requests. Commerce turns them into precise drafts—no follow-ups, no workflow redesign.",
      image: "/generated/image-a-professional-headshot-of-sarah-greene-.webp"
    }
  ]}
/>

<CallToAction
  title="Let your front office run itself"
  subtitle="AI agents purpose-built for wholesale. Automate workflows across sales, ops, support, and finance — with zero lift from your team."
  description="Commerce Systems replaces hours of manual work with intelligent agents that handle your front-office tasks — fast, reliable, and always up to date. Join wholesale leaders cutting costs, speeding up sales, and freeing teams from busywork."
  imageSrc="/generated/image-a-cheerful-wholesale-professional-in-a-m.webp"
  callsToAction={[
    { href: '/demo', label: 'Get a demo', variant: 'primary' },
    { href: '/contact', label: 'Talk to sales', variant: 'secondary' }
  ]}
/>
