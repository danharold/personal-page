<script lang="ts">
	import Button from '$lib/components/ui/button/button.svelte';
	import Separator from '$lib/components/ui/separator/separator.svelte';

	import { Sun, Moon, ChevronRightIcon } from 'lucide-svelte';

	import { toggleMode } from 'mode-watcher';

	import ConsoleTyper from './ConsoleTyper.svelte';
</script>

<header class="w-full">
	<div class="grid w-full grid-cols-3 items-center p-4">
		<a href="/" class="flex justify-self-start font-mono text-lg"><ConsoleTyper /></a>
		<nav class="flex flex-1 justify-center space-x-2">
			<Button variant="ghost" href="/about">About</Button>
			<Button variant="ghost" href="/Blog">Blog</Button>
			<Button variant="ghost" href="#projects">Projects</Button>
			<Button variant="ghost" href="#contact">Contact</Button>
		</nav>
		<div class="flex items-center justify-self-end">
			<span class="text-muted-foreground/20 mr-4 scale-0 text-xs dark:scale-100"
				>⚠ flashbang warning ⚠</span
			>
			<Button
				on:click={toggleMode}
				size="icon"
				class="bg-foreground/80 h-8 w-8 cursor-pointer justify-self-end"
			>
				<Sun class="h-5 w-5 scale-0 dark:scale-100" />
				<Moon class="absolute h-5 w-5 scale-100 dark:scale-0" />
			</Button>
		</div>
	</div>
	<Separator />
</header>
