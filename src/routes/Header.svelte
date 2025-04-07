<script lang="ts">
	import Button from '$lib/components/ui/button/button.svelte';
	import Separator from '$lib/components/ui/separator/separator.svelte';
	import ThemeToggle from './ThemeToggle.svelte';
	import ConsoleTyper from './ConsoleTyper.svelte';
	import { Menu } from 'lucide-svelte';

	import { fly } from 'svelte/transition';

	let isMobileMenuOpen = false;

	function toggleMobileMenu() {
		isMobileMenuOpen = !isMobileMenuOpen;
	}
</script>

<header class="w-full">
	<div class="grid w-full grid-cols-3 items-center p-4">
		<a href="/" class="flex justify-self-start font-mono text-lg"><ConsoleTyper /></a>
		<nav class="hidden flex-1 justify-center space-x-2 md:flex">
			<Button variant="ghost" href="/about">About</Button>
			<Button variant="ghost" href="/Blog">Blog</Button>
			<Button variant="ghost" href="#projects">Projects</Button>
			<Button variant="ghost" href="#contact">Contact</Button>
		</nav>

		<div class="col-start-3 flex items-center justify-self-end md:hidden">
			<Button on:click={toggleMobileMenu} size="icon" class="!h-10 !w-10">
				<Menu class="h-6 w-6" />
			</Button>
		</div>
	</div>
	<Separator />

	{#if isMobileMenuOpen}
		<div transition:fly={{ duration: 300 }}>
			<div class="flex flex-col items-center space-y-2 p-4 md:hidden">
				<Button variant="ghost" href="/about">About</Button>
				<Button variant="ghost" href="/Blog">Blog</Button>
				<Button variant="ghost" href="#projects">Projects</Button>
				<Button variant="ghost" href="#contact">Contact</Button>
				<Separator />
			</div>
		</div>
	{/if}
</header>
