<script lang="ts">
	import Button from '$lib/components/ui/button/button.svelte';
	import Separator from '$lib/components/ui/separator/separator.svelte';

	import { Sun, Moon } from 'lucide-svelte';

	import { toggleMode } from 'mode-watcher';
</script>

<header class="w-full">
	<div class="grid w-full grid-cols-3 items-center p-4">
		<a href="/" class="flex justify-self-start font-mono text-lg">😸 danharold.com</a>
		<nav class="flex flex-1 justify-center space-x-2">
			<Button variant="ghost" href="/about">About</Button>
			<Button variant="ghost" href="/Blog">Blog</Button>
			<Button variant="ghost" href="#projects">Projects</Button>
			<Button variant="ghost" href="#contact">Contact</Button>
		</nav>
		<div class="justify-self-end">
			<Button on:click={toggleMode} size="icon" class="cursor-pointer justify-self-end">
				<Sun class="h-6 w-6 scale-100 dark:scale-0" />
				<Moon class="absolute h-6 w-6 scale-0 dark:scale-100" />
			</Button>
		</div>
	</div>
	<Separator />
</header>
