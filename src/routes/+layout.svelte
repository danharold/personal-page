<script lang="ts">
	import Header from './Header.svelte';
	import Footer from './Footer.svelte';

	import { ModeWatcher } from 'mode-watcher';
	let { children } = $props();
	import '../app.css';
</script>

<div class="mx-auto flex min-h-screen w-full max-w-screen-lg flex-col">
	<ModeWatcher defaultMode={'dark'} />
	<Header />
	<main class="container mx-auto flex min-h-1/2 flex-grow flex-col px-4 py-10">
		{@render children()}
	</main>
	<Footer />
</div>
