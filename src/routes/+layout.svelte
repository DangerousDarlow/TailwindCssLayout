<script lang="ts">
	import '../app.postcss';

	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="flex flex-col">
	<header class="bg-green-800">
		<h1>Header</h1>
	</header>

	<main class="bg-blue-950">
		<div class="space-y-4">
			{@render children?.()}
		</div>
	</main>

	<footer class="bg-red-800">
		<h1>Footer</h1>
	</footer>
</div>
