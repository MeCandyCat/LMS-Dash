<script>
	import { page } from '$app/stores';
	import links from '$lib/links'
</script>

<div class="flex-col h-screen overflow-hidden bg-x center-everything ">
	<h1 class="pb-16 text-5xl font-bold text-center drop-shadow-2xl">{$page?.error?.message || 'Something went wrong...'}</h1>
	<h1 class="text-4xl font-semibold text-center text-indigo-400 drop-shadow-2xl">{$page.status}</h1>
</div>

<footer class="relative flex flex-col items-center justify-around gap-10 p-16 text-lg font-bold bg-slate-950 md:flex-row">
	<div class="text-center">
		<h1 class="text-8xl">LMS</h1>
		<p>&copy LMS Developer Team</p>
	</div>
	<div class="flex gap-10 underline-offset-2">
		<a class="hover:underline" href={links.docsLink} target="_blank">Docs</a>
		<a class="hover:underline" href={links.supportLink} target="_blank">Support</a>
		<a class="hover:underline" href={links.inviteLink} target="_blank">Invite</a>
		<a class="hover:underline" href="/dash">Dashboard</a>
		<a class="hover:underline" href="/terms">Terms</a>
		<a class="hover:underline" href="/privacy">Privacy</a>
	</div>
</footer>