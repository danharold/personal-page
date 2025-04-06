<script lang="ts">
	import { Button } from '$lib/components/ui/button/';
	import * as Card from '$lib/components/ui/card/';
	import { Github, Linkedin, Mail } from 'lucide-svelte';

	const projects = [
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
		// Add more projects
	];
</script>

<div class="dark container mx-auto flex min-h-1/2 flex-col px-4">
	<main class="flex-grow py-10 md:py-16">
		<!-- <section class="mb-16 text-center">
			<h1 class="mb-3 text-4xl font-bold md:text-5xl">Your Name</h1>
			<p class="text-muted-foreground text-lg">
				Web Developer | Minimalist Designer | Svelte Enthusiast
			</p>
		</section> -->

		<!-- <section id="projects">
			<h2 class="mb-8 text-center text-3xl font-semibold md:text-left">Featured Projects</h2>
			<div class="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-3">
				{#each projects as project (project.id)}
					<Card.Root class="overflow-hidden">
						{#if project.image}
							<div class="bg-muted flex aspect-video items-center justify-center">
								<span class="text-muted-foreground text-sm">Image</span>
							</div>
						{/if}
						<Card.Header>
							<Card.Title>{project.title}</Card.Title>
						</Card.Header>
						<Card.Content>
							<Card.Description>{project.description}</Card.Description>
						</Card.Content>
						<Card.Footer>
							<Button variant="link" class="h-auto p-0">Learn More</Button>
						</Card.Footer>
					</Card.Root>
				{/each}
			</div>
		</section>
	</main> -->
	</main>
</div>
