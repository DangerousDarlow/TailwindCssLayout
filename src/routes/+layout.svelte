<script lang="ts">
	import '../app.postcss';

	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="flex flex-col max-w-screen-2xl mx-auto">
	<header class="bg-emerald-800 h-20 fixed top-0 max-w-screen-2xl mx-auto left-0 right-0">
		<h1>Header</h1>
	</header>

	<div class="flex pt-20 pb-20">
		<aside class="bg-yellow-800 w-64 fixed top-20 bottom-20">
			<h1>Aside</h1>
		</aside>

		<main class="bg-blue-900 flex-1 ml-64">
			<div class="space-y-4">
				{@render children?.()}
			</div>
		</main>
	</div>

	<footer class="bg-pink-800 h-20 fixed bottom-0 max-w-screen-2xl mx-auto left-0 right-0">
		<h1>Footer</h1>
	</footer>
</div>
