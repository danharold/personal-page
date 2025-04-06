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
	<div class="py-4">
		<div class="flex justify-center space-x-4">
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
		<p class="text-muted-foreground mt-4 text-center text-sm">
			Dan Harold &copy; {new Date().getFullYear()}
		</p>
	</div>
</footer>
