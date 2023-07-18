<script lang="ts">
	import CTA from '$components/Cta.svelte';
	import { DeviceGamepad2, Music, Old, Tooltip } from 'tabler-icons-svelte';
	import Section from '../lib/components/Section.svelte';

	const clients = [
		{
			name: 'C-Media Solutions',
			website: 'http://c-mediasolutions.com/',
			imageUrl: 'client-c-media.png'
		},
		{
			name: 'Oddvision',
			website: 'https://oddvision.io',
			imageUrl: 'client-oddvision.png'
		}
		// {
		// 	name: 'Universal Music Group',
		// 	website: 'https://www.universalmusic.com/',
		// 	imageUrl: 'client-umg.png'
		// }
	];

	// const projects = [
	// 	{
	// 		title: 'Dawn FM',
	// 		link: 'https://www.oddvision.io/theweeknd',
	// 		description: 'Project description'
	// 	}
	// ];

	const tools = [
		{
			name: 'AWS',
			website: 'https://aws.amazon.com/',
			imageUrl: 'tech-aws.png'
		},
		{
			name: 'Google Cloud',
			website: 'https://cloud.google.com/',
			imageUrl: 'tech-gcp.png'
		},
		{
			name: 'TypeScript',
			website: 'https://www.typescriptlang.org/',
			imageUrl: 'tech-typescript.png'
		},
		{
			name: 'React',
			website: 'https://react.dev/',
			imageUrl: 'tech-react.png'
		},
		{
			name: 'Node',
			website: 'https://nodejs.org/en',
			imageUrl: 'tech-node.png'
		},
		{
			name: 'PostgreSQL',
			website: 'https://www.postgresql.org/',
			imageUrl: 'tech-psql.png'
		},
		{
			name: 'PlayCanvas',
			website: 'https://playcanvas.com/',
			imageUrl: 'tech-playcanvas.png'
		},
		{
			name: 'Unity',
			website: 'https://unity.com/',
			imageUrl: 'tech-unity.png'
		},
		{
			name: 'Redis',
			website: 'https://redis.io/',
			imageUrl: 'tech-redis.png'
		},
		{
			name: 'Kubernetes',
			website: 'https://kubernetes.io/',
			imageUrl: 'tech-k8s.png'
		},
		{
			name: 'Colyseus',
			website: 'https://colyseus.io/',
			imageUrl: 'tech-colyseus.png'
		},
		{
			name: 'Tailwind',
			website: 'https://tailwindcss.com/',
			imageUrl: 'tech-tailwind.png'
		}
	];

	// const testimonials = [
	// 	{
	// 		author: 'Carl Leducq — Project Manager; NZGDA Chairperson',
	// 		summary:
	// 			"You're legends for smashing through and getting this all set up. What would've taken me months took you days!"
	// 	}
	// ];
</script>

<svelte:head>
	<title>KNGFSHR — The dev agency of the future</title>
</svelte:head>

<!-- Hero backgrounds -->
<div class="h-screen w-screen absolute top-0 z-[-1] hero-gradient-bg" />
<div class="h-screen w-screen absolute top-0 z-[-2] hero-gradient-primary" />
<div class="h-screen w-screen absolute top-0 z-[-3] hero-grid-pattern" />

<Section id="hero">
	<div class="max-w-3xl">
		<div class="text-center">
			<h1 class="text-4xl font-bold tracking-tight text-gray-900 sm:text-8xl">
				The dev agency of the future
			</h1>
			<p class="mt-10 md:mt-20 text-md md:text-2xl leading-8">
				We create products and 3D mixed reality experiences that run anywhere
			</p>
			<CTA />
		</div>
	</div>
</Section>

<Section id="partners">
	<h2 class="subtitle">We work with the best</h2>
	<h3>Our partnerships enable awesome work</h3>
	<div class="grid-showcase-clients">
		{#each clients as c}
			<a href={c.website} target="_blank" rel="noreferrer noopener" class="grid-item">
				<img src={c.imageUrl} alt={c.name} class="mx-auto object-cover h-14 md:h-20" />
			</a>
		{/each}
	</div>
</Section>

<Section id="team">
	<div class="max-w-4xl">
		<h2 class="subtitle">A team of experts</h2>
		<h3>Who is KNGFSHR?</h3>
		<p class="paragraph">
			In honour of the <a
				href="https://nzbirdsonline.org.nz/species/sacred-kingfisher"
				target="_blank">Kingfisher bird</a
			>, we're a product development agency born in New Zealand. Our specialty is creating 3D and XR
			experiences that are accessible to everyone
		</p>
		<p class="paragraph">
			We're seasoned professionals who started our careers as game developers, and later pivoted to
			building web products. This gave us a wide range of skills we use on a daily basis
		</p>
		<p class="paragraph">
			With the rise of the future we saw a great opportunity — so we acted. Since then, we've been
			building memorable experiences that support online multiplayer, live music streaming,
			real-time voice chat, and the most important part: interactivity
		</p>
		<CTA />
	</div>
</Section>

<Section id="services">
	<div class="max-w-3xl">
		<h2 class="subtitle">We know our craft</h2>
		<h3>Services we provide</h3>
		<dl
			class="mt-10 grid max-w-xl grid-cols-1 gap-x-8 gap-y-10 lg:max-w-none lg:grid-cols-2 lg:gap-y-16 text-left"
		>
			<div class="relative pl-16">
				<dt class="feature-label">
					<div class="feature-icon-wrapper">
						<DeviceGamepad2 color="white" />
					</div>
					Online Multiplayer Experiences
				</dt>
				<dd class="mt-2 text-base leading-7 text-gray-600">
					We enable real-time online experiences with tools such as Colyseus, GCP, Kubernetes, and
					Redis
				</dd>
			</div>
			<div class="relative pl-16">
				<dt class="feature-label">
					<div class="feature-icon-wrapper">
						<Music color="white" />
					</div>
					Music Streaming
				</dt>
				<dd class="mt-2 text-base leading-7 text-gray-600">
					Get access to a brand new distribution channels by integrating Spotify, Apple Music to
					your experiences
				</dd>
			</div>
			<div class="relative pl-16">
				<dt class="feature-label">
					<div class="feature-icon-wrapper">
						<Tooltip color="white" />
					</div>
					Guided / Musical tours
				</dt>
				<dd class="mt-2 text-base leading-7 text-gray-600">
					Showcase your idea / work with an interactive tour that takes you through different stops
				</dd>
			</div>
			<div class="relative pl-16">
				<dt class="feature-label">
					<div class="feature-icon-wrapper">
						<Old color="white" />
					</div>
					Walking simulators
				</dt>
				<dd class="mt-2 text-base leading-7 text-gray-600">
					Give users the ability to roam freely through different worlds, connecting with your brand
					on a new level
				</dd>
			</div>
		</dl>
		<p class="mt-16 text-md md:text-lg text-gray-500 max-w-xl text-center mx-auto">
			Note: Our projects normally involve more than 1 of the features listed below. We've developed
			tools that help us integrate these easily
		</p>
		<CTA />
	</div>
</Section>

<Section id="tech">
	<h2 class="subtitle">Great tools — fast delivery times</h2>
	<h3>We use cutting edge technology</h3>
	<div class="max-w-4xl">
		<p class="paragraph">
			In order to build the most accessible products, we knew the web was the place to be at. Most
			of our experiences run on web browsers so we leverage the power of today's computers
		</p>
	</div>
	<div class="grid-showcase-tech">
		{#each tools as t}
			<a href={t.website} target="_blank" rel="noreferrer noopener" class="grid-item">
				<img src={t.imageUrl} alt={t.name} class="mx-auto object-cover h-12 md:h-16" />
			</a>
		{/each}
	</div>
	<CTA />
</Section>

<!-- <section id="testimonials">
	<h2>Our work speaks for itself</h2>
	{#each testimonials as testimonial}
		<div class="max-w-md">
			<p class="mb-2">{testimonial.summary}</p>
			<p class="text-gray-500">{testimonial.author}</p>
		</div>
	{/each}
	<CTA />
</section> -->

<footer>
	<p>
		© 2023 KNGFSHR
		<!-- — Built by
		<a href="https://timrodz.dev">timrodz</a> with
		<a href="https://svelte.dev/" target="_blank">Svelte</a> -->
	</p>
</footer>

<style lang="postcss">
	footer {
		@apply mt-16;
	}

	h2 {
		@apply mb-4 font-bold text-indigo-500 text-xl;
	}

	h3 {
		@apply mb-10 text-center text-2xl md:text-4xl font-semibold leading-8 text-gray-900;
	}

	.hero-gradient-bg {
		background: linear-gradient(1turn, hsla(0, 0%, 85%, 0) 27.6%, #fff);
		transform: rotate(-180deg);
	}

	.hero-gradient-primary {
		background: radial-gradient(
			68.14% 121.75% at 50% 50%,
			hsla(0, 0%, 100%, 0) 0,
			rgba(221, 205, 252, 0.49) 100%
		);
		transform: rotate(-180deg);
	}

	.hero-grid-pattern {
		background-size: 6rem 4rem;
		background-image: linear-gradient(90deg, #f0f0f0 1px, transparent 0),
			linear-gradient(180deg, #efeded 1px, transparent 0);
	}

	.paragraph {
		@apply mt-10 md:mt-6 leading-7 md:text-xl md:leading-[2.5rem];
	}

	.grid-showcase-clients {
		@apply mx-auto mt-16 mb-16 grid max-w-lg grid-cols-1 md:grid-cols-2 items-center md:gap-x-6 gap-y-14 sm:max-w-xl sm:gap-x-10 lg:mx-0 lg:max-w-none;
	}

	.grid-showcase-tech {
		@apply mx-auto mt-16 mb-16 grid max-w-lg grid-cols-1 md:grid-cols-3 items-center md:gap-x-6 gap-y-14 sm:max-w-xl sm:gap-x-10 lg:mx-0 lg:max-w-none;
	}

	.grid-item {
		@apply col-span-2 w-full object-contain lg:col-span-1;
	}

	.feature-label {
		@apply text-base font-semibold leading-7 text-gray-900;
	}

	.feature-icon-wrapper {
		@apply absolute left-0 top-0 flex h-10 w-10 items-center justify-center rounded-lg bg-gray-600;
	}
</style>
