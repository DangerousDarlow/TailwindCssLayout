<script lang="ts">
	import '../app.postcss';

	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="flex flex-col max-w-screen-2xl mx-auto">
	<header class="bg-green-800 h-20 fixed top-0 max-w-screen-2xl mx-auto left-0 right-0">
		<h1>Header</h1>
	</header>

	<main class="bg-blue-950 pt-24 pb-24">
		<div class="space-y-4">
			{@render children?.()}
		</div>
	</main>

	<footer class="bg-red-800 h-20 fixed bottom-0 max-w-screen-2xl mx-auto left-0 right-0">
		<h1>Footer</h1>
	</footer>
</div>
