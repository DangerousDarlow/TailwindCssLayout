<script lang="ts">
	import '../app.postcss';

	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="flex flex-col max-w-screen-2xl mx-auto">
	<header class="bg-red-500 bg-opacity-40 fixed top-0 left-0 right-0 h-20 max-w-screen-2xl mx-auto">
		<h1 class="flex items-center justify-center inset-0 absolute">Header</h1>
	</header>

	<div class="flex pt-20 pb-20">
		<aside
			class="bg-green-500 bg-opacity-40 fixed top-20 bottom-0 md:bottom-20 w-64 hidden md:block"
		>
			<h1>Aside</h1>
		</aside>

		<main class="bg-blue-500 bg-opacity-40 flex-1 md:ml-64">
			<div class="space-y-4">
				{@render children?.()}
			</div>
		</main>
	</div>

	<footer class="bg-default fixed bottom-0 left-0 right-0 h-20 max-w-screen-2xl mx-auto">
		<h1 class="flex items-center justify-center inset-0 absolute">Footer</h1>
	</footer>
</div>
