<script lang="ts">
	import Button from '$lib/components/ui/button/button.svelte';
	import { Sun, Moon } from 'lucide-svelte';
	import { toggleMode, mode } from 'mode-watcher';
</script>

<Button
	on:click={toggleMode}
	size="icon"
	class="bg-foreground/80 !h-10 !w-10 cursor-pointer justify-self-end"
>
	<Sun class="h-6 w-6 scale-0 dark:scale-100" />
	<Moon class="absolute h-6 w-6 scale-100 dark:scale-0" />
</Button>
