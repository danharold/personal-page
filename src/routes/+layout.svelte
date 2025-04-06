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
	<main class="flex-grow">
		{@render children()}
	</main>
	<Footer />
</div>
