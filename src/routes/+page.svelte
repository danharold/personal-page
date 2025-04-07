<script lang="ts">
	import Button from '$lib/components/ui/button/button.svelte';
	import * as Card from '$lib/components/ui/card/index.js';
	import { ArrowRight } from 'lucide-svelte';
	import * as Carousel from '$lib/components/ui/carousel/index.js';

	const featured_projects = [
		{
			id: 1,
			title: 'Project One',
			description: 'A short description.',
			image: '/images/project1.jpg'
		},
		{
			id: 2,
			title: 'Project Two',
			description: 'Another cool project.',
			image: '/images/project2.jpg'
		},
		{
			id: 3,
			title: 'Project Three',
			description: 'Minimalist design study.',
			image: '/images/project3.jpg'
		},
		{
			id: 4,
			title: 'Project Four',
			description: 'SvelteKit exploration.',
			image: '/images/project4.jpg'
		}
	];
</script>

<!-- <h1 class="text-4xl font-bold">Dan Harold</h1>
	<p class="text-muted-foreground text-lg">Full-Stack Developer & Data Enthusiast</p>
	<div class="flex flex-row space-x-2">
		<MapPin strokeWidth={0.8} size={24} />
		<p class="text-muted-foreground text-lg">United Kingdom</p>
	</div>

	<p>
		Building innovative web applications and data-driven solutions with Python and modern web
		technologies.
	</p> -->

<section class="my-auto h-full w-full items-center justify-center text-center">
	<div>
		<h1 class="mb-0 text-6xl font-bold">Dan Harold</h1>
		<p class=" text-muted-foreground mb-6">Full-Stack Developer | Data Enthusiast</p>
		<p class="text-foreground text-xl">
			Building web applications and data-driven solutions using Python and modern web technologies.
			I enjoy solving problems and learning new stuff to build cool things. Always learning, always
			creating.
		</p>
	</div>
	<!-- <div class="bg-foreground m-10 h-50">
		<p class=" text-muted-foreground">Central Placeholder</p>
	</div> -->
	<Carousel.Root class="mx-20 my-10">
		<Carousel.Content>
			{#each featured_projects as proj}
				<Carousel.Item class="md:basis-1/2 lg:basis-1/3"
					><div class="">
						<Card.Root>
							{#if proj.image}
								<div class="bg-muted flex aspect-video items-center justify-center">
									<span class="text-muted-foreground text-sm">Image</span>
								</div>
							{/if}
							<Card.Header>
								<Card.Title>{proj.title}</Card.Title>
							</Card.Header>
							<Card.Content>
								<Card.Description>{proj.description}</Card.Description>
							</Card.Content>
							<Card.Footer>
								<Button variant="link" class="h-auto p-0">Learn More</Button>
							</Card.Footer>
						</Card.Root>
					</div></Carousel.Item
				>
			{/each}
		</Carousel.Content>
		<Carousel.Previous />
		<Carousel.Next />
	</Carousel.Root>

	<Button variant="outline" class="text-foreground rounded-full p-4" href="/projects">
		View all of my projects
	</Button>
</section>
