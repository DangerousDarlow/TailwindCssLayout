<script lang="ts">
	import '../app.postcss';

	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="flex flex-col px-4 max-w-7xl mx-auto min-h-screen">
	<main>
		<div class="flex-1 space-y-4 overflow-y-auto">
			{@render children?.()}
		</div>
	</main>
</div>
