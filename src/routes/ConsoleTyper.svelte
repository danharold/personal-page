<script lang="ts">
	import { onMount } from 'svelte';

	let text = '> ';
	let cursor = '_';
	let currentIndex = 0;

	async function typeMessage(message: string): Promise<void> {
		return new Promise((resolve) => {
			let messageIndex = 0;
			const typingInterval = setInterval(() => {
				if (messageIndex < message.length) {
					text += message[messageIndex];
					messageIndex++;
				} else {
					clearInterval(typingInterval);
					setTimeout(() => {
						resolve();
					}, 1000);
				}
			}, 200);
		});
	}

	async function deleteMessage(message: string): Promise<void> {
		return new Promise((resolve) => {
			const deletingInterval = setInterval(() => {
				if (currentIndex > 0) {
					currentIndex--;
					if (currentIndex > 0) {
						text = '> ' + message.substring(0, currentIndex);
					} else {
						text = '> ';
					}
				} else {
					clearInterval(deletingInterval);
					resolve();
				}
			}, 50);
		});
	}

	function shuffleArray(array: string[]): string[] {
		for (let i = array.length - 1; i > 0; i--) {
			const j = Math.floor(Math.random() * (i + 1));
			const temp = array[i];
			array[i] = array[j];
			array[j] = temp;
		}
		return array;
	}

	async function typeMessages(messages: string[]): Promise<void> {
		const shuffledMessages = shuffleArray(messages);
		for (const message of shuffledMessages) {
			// type webpage url first
			const webpageUrl = 'danharold.com';
			await typeMessage(webpageUrl);
			currentIndex = webpageUrl.length; // set currentIndex before deleting
			await deleteMessage(webpageUrl);

			// then type one of the messages
			await new Promise((resolve) => setTimeout(resolve, 2500));
			await typeMessage(message);
			currentIndex = message.length; // set currentIndex before deleting
			await deleteMessage(message);
			await new Promise((resolve) => setTimeout(resolve, 2500));
		}
		typeMessages(messages); // loop messages
	}

	onMount(() => {
		const cursorInterval = setInterval(() => {
			cursor = cursor === '_' ? ' ' : '_';
		}, 500);

		const messages = [
			'Hello!',
			'Welcome!',
			'Nice to see you',
			'make coffee',
			'kill -9 procrastination',
			"grep 'TODO' *.js | wc -l",
			"alias please='sudo'",
			'yes | rm -rf /',
			'npm i motivation',
			'¯\\_(ツ)_/¯',
			'(╯°□°）╯︵ ┻━┻',
			':D :> ^_^ c: >:]'
		];

		typeMessages(messages);

		return () => clearInterval(cursorInterval);
	});
</script>

<span class="overflow-x-visible font-mono text-lg whitespace-nowrap">{text}{cursor}</span>
