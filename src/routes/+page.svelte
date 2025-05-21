<script lang="ts">
	// Components
	import UseCases from "$lib/components/layout/UseCases.svelte";
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import CustomerCardHero from "$lib/components/layout/hero-sections/CustomerCardHero.svelte";
</script>

<CustomerCardHero
  title="Let your front office run itself"
  subtitle="Commerce Systems automates everyday work across sales, support, operations, and finance—so your wholesale business runs faster with fewer headaches."
  centered={false}
  customers={[
    {
      name: 'Mark Ramsey',
      position: 'director of operations, Artisan Beverage Distributors',
      imageSrc: '/generated/image-a-male-director-mark-ramsey-in-a-beverag.webp'
    },
    {
      name: 'Lisa Chen',
      position: 'sales manager, Pacific Pet Supply',
      imageSrc: '/generated/image-a-female-sales-manager-lisa-chen-in-a-pe.webp'
    },
    {
      name: 'Carlos Rivera',
      position: 'VP of finance, Horizon Electronics Wholesale',
      imageSrc: '/generated/image-a-male-vp-of-finance-carlos-rivera-in-an.webp'
    },
    {
      name: 'Sarah Jennings',
      position: 'head of customer support, Willow Grove Home Furnishings',
      imageSrc: '/generated/image-a-female-head-of-customer-support-sarah-.webp'
    },
    {
      name: 'Dwayne Mitchell',
      position: 'operations lead, Triangle Apparel Group',
      imageSrc: '/generated/image-a-male-operations-lead-dwayne-mitchell-i.webp'
    }
  ]}
/>
<LogoScroller
	label="Trusted by industry leaders"
	logoUrls={[
		'https://logo.clearbit.com/unfi.com',
		'https://logo.clearbit.com/kehe.com',
		'https://logo.clearbit.com/genco.com',
		'https://logo.clearbit.com/rexelusa.com'
	]}
/>

<Summary
	title="AI agents for wholesale front offices"
	text="Commerce Systems builds AI agents that automate sales, operations, support, and finance workflows for wholesale manufacturers and distributors. Free your team from manual busywork and reduce operational costs—no extra hiring required."
/>

<Testimonials
	testimonials={[
		{
			name: "Martin Rozman",
			position: "director of operations",
			company: "Elemental Supply",
			quote:
				"We got 600 hours a month back. It’s like giving each person on my team 20 hours a week to focus on high-value work again.",
			image:
				"/generated/image-a-male-operations-director-in-a-bustling.webp"
		},
		{
			name: "Lena Kapur",
			position: "vp of finance",
			company: "Delco Foods",
			quote:
				"We used to spend days cleaning up buyer POs. One missed digit could affect hundreds of units. Commerce catches mistakes before they hit the ERP—and before they hit our margins.",
			image:
				"/generated/image-a-female-finance-vice-president-in-a-con.webp"
		},
		{
			name: "Robert Chi",
			position: "head of customer experience",
			company: "Galaxy Apparel Collective",
			quote:
				"We reduced support headcount by 40%—without slowing responses. The agent handles the repetitive stuff, so our human team handles the real edge cases.",
			image:
				"/generated/image-a-male-customer-support-leader-in-an-ope.webp"
		}
	]}
/>

<Features
	title="Built to automate the wholesale front office"
	subtitle="Six ways Commerce Systems delivers value for manufacturers and distributors"
	features={[
		{
			title: "AI agents for every department",
			description: "Automate sales, support, ops, and finance tasks with purpose-built AI that fits your existing business." 
		},
		{
			title: "Fast setup, zero technical lift",
			description: "Go live in one week, no internal engineers or developers needed—we handle setup for you." 
		},
		{
			title: "Works with your legacy systems",
			description: "Syncs directly to SAP, Oracle, Netsuite, Infor, and spreadsheets—no rip-and-replace required." 
		},
		{
			title: "Turns emails into purchase orders",
			description: "Converts messy buyer requests into accurate POs instantly, saving hours of copying and pasting." 
		},
		{
			title: "Real workforce savings",
			description: "Cut support costs by up to 80%—just like our customer Silverpoint Technologies." 
		},
		{
			title: "Measurable productivity gains",
			description: "Teams get daily hours back with automated processes—so your staff focuses on what moves the business forward." 
		}
	]}
/>

<UseCases
	title="Use Cases"
	subtitle="Real-world applications for your business needs"
	useCases={[
		{
			title: "AI-powered customer support",
			description: "Handle hundreds of order status requests, returns, and product questions automatically. Commerce Systems' AI understands your sales history and ERP data to resolve repetitive support tickets—so your staff can focus on high-value conversations.",
			image: "/generated/image-a-bustling-customer-support-team-in-a-mo.webp",
			link: {
				href: "/use-cases/ai-customer-support",
				label: "Learn more"
			}
		},
		{
			title: "Automated off-price sales",
			description: "Stop excess inventory from eating into margins. Our AI agents run clearance pricing checks, review aging stock, and generate verified bulk offers—getting slow-moving goods out the door before they impact your bottom line.",
			image: "/generated/image-a-wholesale-operations-manager-in-a-live.webp",
			link: {
				href: "/use-cases/automated-off-price-sales",
				label: "Learn more"
			}
		},
		{
			title: "Error-free purchase orders",
			description: "Transform messy buyer emails into accurate, ERP-ready purchase orders. Commerce Systems' AI parses requests, validates details, and submits compliant POs—reducing costly mistakes and manual rework for your finance team.",
			image: "/generated/image-a-finance-professional-in-a-wholesale-co.webp",
			link: {
				href: "/use-cases/error-free-purchase-orders",
				label: "Learn more"
			}
		}
	]}
/>

<AboutTeaser />
<CallToAction
  title="Let your front office run itself"
  subtitle="Cut costs, boost speed—all without adding headcount"
  description="Commerce Systems builds AI agents for wholesale manufacturers and distributors, replacing hours of manual work with minutes of automation. Plug in pilots, fast ROI, and no need to overhaul your systems. Start with a pilot—schedule your demo today."
  imageSrc="/generated/image-a-cheerful-wholesale-manufacturing-execu.webp"
  callsToAction=[
    { href: '/contact', label: 'Schedule a demo', variant: 'primary' },
    { href: '/about', label: 'How it works', variant: 'secondary' }
  ]
/>
