<script context="module">
	export const load = async ({ fetch }) => {
		const res = await fetch("/api");
		const data = await res.json();
		console.log(data);

		return {
			props: {
				data,
			},
		};
	};
</script>

<script>
	export let data;
	import Counter from '$lib/Counter.svelte';
</script>

<pre>{JSON.stringify(data)}</pre>

<div class="p-4 mx-auto text-center">
	<h1
		class="max-w-xs mx-auto my-16 text-6xl font-thin text-red-500 uppercase sm:max-w-none"
	>
	Hello<!-- {JSON.stringify(data)} -->
	</h1>

	<Counter />
	<p class="max-w-xs mx-auto my-8 sm:max-w-none">
		Visit the <a href="https://svelte.dev">svelte.dev</a> to learn how to build Svelte
		apps.
	</p>
</div>
