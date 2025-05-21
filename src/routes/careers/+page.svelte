<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
  {
    title: "High-impact roles",
    description: "Work at the intersection of AI and supply chain, where every project helps reshape $8T of wholesale activity.",
    icon: IconBriefcase
  },
  {
    title: "Equity & ownership",
    description: "Every team member receives meaningful equity and direct input into company direction.",
    icon: IconUsers
  },
  {
    title: "Work-life autonomy",
    description: "Flexible remote/hybrid work, open vacation, and a focus on outcomes—not face time.",
    icon: IconHeart
  }
];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
  {
    name: "Simone Carter",
    position: "Product Manager",
    company: "Product Team",
    quote:
      "At Commerce Systems, my ideas are truly valued and I’m empowered to lead projects that have a direct impact on our customers. The culture is open and supportive—people from all backgrounds are encouraged to bring their best. It’s a place where your work matters and your voice is heard.",
    image: "/generated/image-a-mid-career-black-woman-product-manager.webp"
  },
  {
    name: "Javier Castillo",
    position: "Operations Coordinator",
    company: "Operations Team",
    quote:
      "From day one, I was trusted to take on real responsibilities and ask questions. My managers want to help me grow, and there’s always someone willing to show you the ropes. I’ve learned so much already and enjoy coming to work every day.",
    image: "/generated/image-an-early-career-latino-man-operations-co.webp"
  },
  {
    name: "David Lin",
    position: "Engineering Director",
    company: "Engineering Team",
    quote:
      "Commerce Systems is all about collaboration and moving fast together. We solve complex problems, but everyone—from interns to the founders—chips in with ideas and feedback. The flexibility and genuine care for wellbeing here set us apart from anywhere else I’ve worked.",
    image: "/generated/image-a-senior-asian-american-man-engineering-.webp"
  }
];

	const processSteps = [
  {
    step: 1,
    title: "Simple application",
    description: "Send us your info—no need for a lengthy cover letter. Every application is reviewed by a real person."
  },
  {
    step: 2,
    title: "Founder conversation",
    description: "Have a 30-minute conversation about your background, motivation, and fit."
  },
  {
    step: 3,
    title: "Practical challenge",
    description: "Complete a lightweight take-home exercise based on the role—show us how you solve real problems."
  },
  {
    step: 4,
    title: "Meet the team",
    description: "Join a collaborative session with teammates from engineering, product, or ops. Get a true picture of our culture."
  },
  {
    step: 5,
    title: "Offer & feedback",
    description: "Receive a decision and thoughtful feedback—usually within two weeks (often faster)."
  }
];

	const values = [
  {
    icon: IconHeart,
    title: "Candor & context",
    description: "We value open, direct feedback and strong context for bold decision-making—no babysitting."
  },
  {
    icon: IconUsers,
    title: "Weekly shipping",
    description: "Shipping product and learning with customers every week. Your work ships—fast."
  },
  {
    icon: IconGlobe,
    title: "Results, not rank",
    description: "Everyone owns outcomes, contributes ideas, and helps one another grow. Title doesn’t matter, impact does."
  }
];
</script>

<!-- Hero Section -->

<SecondaryHero
  title="Shape the future of wholesale"
  subtitle="Build world-class AI with a real-world impact. Join a fast-moving team where your work drives meaningful change for America's wholesale economy. You'll solve hard problems, learn quickly, and collaborate across disciplines to reinvent how critical business gets donefrom sales and support to operations and finance."
  imageSrc="/generated/image-a-modern-startup-office-with-a-diverse-t.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Build your career while making an impact" />

	<div class="mt-16 grid gap-4 md:grid-cols-3">
		{#each benefits as benefit}
			<Card {...benefit} />
		{/each}
	</div>
</section>

<!-- Culture Section -->
<Culture {values} />

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>
