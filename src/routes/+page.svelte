<script lang="ts">
	import Client from '$components/Client.svelte';
	import CTA from '$components/Cta.svelte';
	import Project from '$components/Project.svelte';

	// TODO: Add images
	const clients = [
		{
			name: 'C-Media Solutions',
			website: '',
			imageUrl: ''
		},
		{
			name: 'Universal Music Group',
			website: '',
			imageUrl: ''
		},
		{
			name: 'Oddvision',
			website: 'https://oddvision.io',
			imageUrl: ''
		}
	];

	const projects = [
		{
			title: 'Dawn FM',
			link: 'https://www.oddvision.io/theweeknd',
			description: 'Project description'
		}
	];

	const tools = [
		{
			name: 'TypeScript',
			url: '',
			imageUrl: ''
		},
		{
			name: 'React',
			url: '',
			imageUrl: ''
		},
		{
			name: 'Node',
			url: '',
			imageUrl: ''
		},
		{
			name: 'Express',
			url: '',
			imageUrl: ''
		},
		{
			name: 'PlayCanvas',
			url: '',
			imageUrl: ''
		},
		{
			name: 'Unity',
			url: '',
			imageUrl: ''
		}
	];

	const testimonials = [
		{
			author: 'Carl Leducq — Project Manager; NZGDA Chairperson',
			summary:
				"You're legends for smashing through and getting this all set up. What would've taken me months took you days!"
		},
		{
			author: 'Phil Roigard — Head of Technology',
			summary: 'Great job guys'
		}
	];

	const teamMembers = [
		{
			name: 'Juan Morais',
			role: 'Partnerships, 3D, UI/UX'
		},
		{
			name: 'Philip Roigard',
			role: 'Software Architecture, DevOps, Web 3.0'
		}
	];
</script>

<svelte:head>
	<title>KNGFSHR — The dev agency of the metaverse</title>
</svelte:head>

<section id="hero">
	<h1 class="text-3xl md:text-5xl font-bold mb-8">
		Creating 3D experiences that run on any device is our specialty
	</h1>
	<h2 class="text-xl md:text-3xl">
		We build products that support online multiplayer, real-time voice chat, music streaming, and
		analytics. You name the requirements, we'll sort it out.
	</h2>
	<h2 class="section-h2 mt-20">These are our awesome clients & partners</h2>
	<!-- <div class="flex space-x-4"> -->
	{#each clients as c}
		<Client name={c.name} website={c.website} imageUrl={c.imageUrl} />
	{/each}
	<!-- </div> -->
	<CTA />
</section>

<section id="projects">
	<h2 class="section-h2">See our work</h2>
	<p class="text-gray-500 mb-4">
		Note: The nature of this work requires strict NDAs, which means we can't publicly show
		everything we're working on
	</p>
	{#each projects as p}
		<Project title={p.title} link={p.link} description={p.description} />
	{/each}
	<CTA />
	<h2>This is our tech stack</h2>
	<p class="mb-4">
		It changes based on project requirements, but these tools let us spin up work quickly
	</p>
	<!-- TODO: prevent overflow -->
	<div class="grid gap-4">
		{#each tools as tool}
			<a href={tool.url}><img src={tool.imageUrl} alt={tool.name} /></a>
		{/each}
	</div>
</section>

<section id="testimonials">
	<h2 class="section-h2">Our work speaks for itself</h2>
	<!-- <div class="flex flex-col md:flex-row"> -->
	{#each testimonials as testimonial}
		<div class="max-w-sm">
			<p class="mb-2">{testimonial.summary}</p>
			<p class="text-gray-500">{testimonial.author}</p>
		</div>
	{/each}
	<!-- </div> -->
	<CTA />
</section>

<section id="team">
	<h2 class="section-h2">Who are we?</h2>
	<p>
		Since the rise of the Metaverse, we've capitalized on building online, web-based 3D experiences
		that very require niche skillsets, such as ours!
	</p>
	<p>
		We started our careers as game developers, and later pivoted to web products. The technologies
		we dominate are TypeScript, React, Node, Express, PostgreSQL, AWS (web); PlayCanvas and Unity
		(3D)
	</p>
	<h4>Meet the team!</h4>
	{#each teamMembers as member}
		<div class="my-4">
			<p>{member.name}</p>
			<img src="" alt={`Image of ${member.name}`} />
			<p>Specializes in: {member.role}</p>
		</div>
	{/each}
</section>

<footer>
	<p>Made by <a href="https://timrodz.dev">kngfshr</a></p>
</footer>

<style lang="postcss">
	section {
		@apply mb-16;
	}
	.section-h2 {
		@apply font-bold;
	}
</style>
