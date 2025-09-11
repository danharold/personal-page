<script lang="ts">
	import Button from '$lib/components/ui/button/button.svelte';
	import * as Card from '$lib/components/ui/card/index.js';
	import * as Carousel from '$lib/components/ui/carousel/index.js';

	import Autoplay from 'embla-carousel-autoplay';

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

<section class="my-auto h-full w-full items-center justify-center text-center">
	<div>
		<h1 class="mb-0 text-6xl font-bold">Dan Harold</h1>
		<p class=" text-muted-foreground mb-6">Full-Stack Developer | Data Enthusiast</p>
		<p class="text-foreground text-xl">
			Building web applications and data-driven solutions using Python and modern web technologies.
		</p>
	</div>
	<Carousel.Root class="mx-10 my-10" plugins={[Autoplay({ delay: 5000 })]}>
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
