<script>
	import { page } from '$app/stores';
	import links from '$lib/links';
</script>

<div class="bg-x center-everything h-screen flex-col overflow-hidden">
	<h1 class="pb-16 text-center text-5xl font-bold drop-shadow-2xl">{$page?.error?.message || 'Something went wrong...'}</h1>
	<h1 class="text-center text-4xl font-semibold text-indigo-400 drop-shadow-2xl">{$page.status}</h1>
</div>