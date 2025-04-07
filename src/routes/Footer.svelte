<script lang="ts">
	import Button from '$lib/components/ui/button/button.svelte';
	import Separator from '$lib/components/ui/separator/separator.svelte';
	import { GithubIcon, Mail } from 'lucide-svelte';
	import ThemeToggle from './ThemeToggle.svelte';
</script>

<footer id="contact" class="w-full">
	<Separator />

	<div class="grid w-full grid-cols-3 items-center p-4">
		<div class="">
			<Button variant="outline" size="icon">
				<a href="https://github.com/danharold" target="_blank" aria-label="GitHub"
					><GithubIcon strokeWidth={0.8} size={24} />
				</a>
			</Button>
			<Button variant="outline" size="icon">
				<a href="mailto:dan@danharold.com" aria-label="Email"
					><Mail strokeWidth={0.8} size={24} /></a
				>
			</Button>
		</div>
		<p class="text-muted-foreground text-center text-sm">
			&copy; {new Date().getFullYear()} danharold.com
		</p>

		<ThemeToggle />
	</div>
</footer>
