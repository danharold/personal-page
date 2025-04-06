<script lang="ts">
	import Button from '$lib/components/ui/button/button.svelte';
	import Separator from '$lib/components/ui/separator/separator.svelte';
	import { GithubIcon, Mail, MapPin } from 'lucide-svelte';
</script>

<!-- <footer>
	<Separator />
	<div class="bg-background flex w-full max-w-screen-lg content-center items-center px-2 py-5">
		<p>danharold.com &copy {new Date().getFullYear()}</p>
	</div>
</footer> -->

<!-- <footer id="contact" class="text-center">
	<Separator />
	<div class="py-4 text-center">
		<p class="text-muted-foreground mb-4">Get in touch:</p>
		<div class="flex justify-center space-x-4">
			<Button variant="outline" size="icon">
				<a href="/" target="_blank" aria-label="GitHub"><Github strokeWidth={1} /> </a>
			</Button>
			<Button variant="outline" size="icon">
				<a href="/" target="_blank" aria-label="LinkedIn"><Linkedin strokeWidth={1} /></a>
			</Button>
			<Button variant="outline" size="icon">
				<a href="mailto:dan@danharold.com" aria-label="Email"><Mail strokeWidth={1} /></a>
			</Button>
		</div>
		<p class="text-muted-foreground mt-6 text-sm">&copy; {new Date().getFullYear()} Dan Harold</p>
	</div>
</footer> -->

<footer id="contact">
	<Separator />
	<div class="px-6 py-4">
		<div class="text-muted-foreground flex flex-col space-y-4">
			<div class="flex flex-row items-center space-x-2">
				<MapPin strokeWidth={1.5} size={16} class="text-foreground" />
				<p class="font-sans text-xs">United Kingdom</p>
			</div>
			<div class="flex flex-row items-center space-x-2">
				<GithubIcon strokeWidth={1.5} size={16} class="text-foreground" />
				<p class="font-sans text-xs">github.com/danharold</p>
			</div>
			<div class="flex flex-row items-center space-x-2">
				<Mail strokeWidth={1.5} size={16} class="text-foreground" />
				<p class="font-sans text-xs">dan@danharold.com</p>
			</div>
		</div>

		<!-- <div class="flex justify-center space-x-4">
			<Button variant="outline" size="icon">
				<a href="/" target="_blank" aria-label="GitHub"><Github strokeWidth={1} /> </a>
			</Button>
			<Button variant="outline" size="icon">
				<a href="/" target="_blank" aria-label="LinkedIn"><Linkedin strokeWidth={1} /></a>
			</Button>
			<Button variant="outline" size="icon">
				<a href="mailto:dan@danharold.com" aria-label="Email"><Mail strokeWidth={1} /></a>
			</Button>
		</div> -->
		<p class="text-muted-foreground mt-6 text-center text-sm">
			Dan Harold &copy; {new Date().getFullYear()}
		</p>
	</div>
</footer>
