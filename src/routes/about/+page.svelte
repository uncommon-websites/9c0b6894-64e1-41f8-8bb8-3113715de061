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
];
</script>

<SecondaryHero
	title="Transforming wholesale with AI agents"
	subtitle="Automating front-office work so your team can do more"
	imageSrc="/mockups/airport-screen-1747848616457.png"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"For most wholesale manufacturers and distributors, the front office is running on duct tape. Teams are stuck forwarding emails, downloading spreadsheets, and poking around outdated ERPs just to keep basic operations afloat. Buying teams are getting more demanding, costs are rising, and the work keeps piling up. Executives know things need to change, but most mid-market companies don’t have a deep bench of engineers or data analysts to fix it.",
		"Joe Betesh and Aaron Shakib saw this all too clearly. Joe comes from four generations of retail, ran strategy and operations at OpenStore, and worked with dozens of brands still held back by manual workflows. Aaron built demand planning tools and worked on distributed systems at Hubspot. They kept hitting the same wall: front-office teams were overextended, disconnected from their systems, and drowning in busywork—because tools meant for other industries didn’t fit wholesale.",
		"That’s why they started Commerce Systems. The company builds AI agents designed for wholesalers—starting with customer service, operations, sales, and finance. Within five months, the solution helped a customer cut 80% of support work, signed hundred-thousand-dollar contracts, and proved that fast, lean automation is possible even without massive IT departments. The goal is simple: give frontline teams better tools, and give busy companies back their time."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
  stakeholderType="team"
  title="Our team."
  subtitle="Meet our founders."
  stakeholders={[
    {
      name: "Joe Betesh",
      position: "Co-founder & CEO",
      bio: "Data science and finance background, product designer, fourth-generation retailer, former head of ops at OpenStore.",
      image: "/generated/image-a-headshot-of-a-middle-aged-man-with-a-d.webp"
    },
    {
      name: "Aaron Shakib",
      position: "Co-founder & CTO",
      bio: "Distributed systems engineer, ex-Hubspot and OpenStore, built demand and inventory platforms.",
      image: "/generated/image-a-headshot-of-a-young-man-with-a-direct-.webp"
    }
  ]}
/>

<StakeholderGrid
	stakeholderType="investor"
	title="Backed by the best."
	subtitle="Point Nine, TSIC and others"
	stakeholders={[
		{
			name: "Point Nine Capital",
			image: "https://cdn.brandfetch.io/pointnine.com/w/400/h/400/logo?c=1id_elLz2Bd5Ej-dWo7"
		},
		{
			name: "TSIC Ventures",
			image: "https://cdn.brandfetch.io/tiny.vc/w/400/h/400/logo?c=1a2b3c4d5e"
		},
		{
			name: "Sequoia Capital",
			image: "https://cdn.brandfetch.io/sequoiacap.com/w/400/h/400/logo"
		}
	]}
/>

<!-- CTA Section -->
<CallToAction
  title="Build software where every launch matters"
  subtitle="Join the team at Commerce Systems"
  description="We’re pragmatic engineers, product thinkers, and operators fixing the $600B problem of front-office manual work in wholesale. Want to help? Bring your curiosity, drive, and desire to make things truly work—for real customers. Not here for startup theater? Neither are we. Ready to work where outcomes come first? Email us at jobs@commercesystems.com."
  imageSrc="/uploaded/happy-diverse-team-wholesale.jpg"
  callsToAction={[
    {
      href: 'mailto:jobs@commercesystems.com',
      label: 'Email us to apply',
      variant: 'primary',
    },
  ]}
/>
