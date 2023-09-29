<script>
	import { page } from '$app/stores';
	import links from '$lib/links'
    import { base } from '$app/paths';
</script>

<div class="flex-col h-screen overflow-hidden bg-x center-everything ">
	<h1 class="pb-16 text-5xl font-bold text-center drop-shadow-5xl">COMING SOON</h1>
</div>

<footer class="relative flex flex-col items-center justify-around gap-10 p-16 text-lg font-bold bg-slate-950 md:flex-row">
	<div class="text-center">
		<h1 class="text-8xl">LMS</h1>
		<p>&copy LMS Developer Team</p>
	</div>
	<div class="flex gap-10 underline-offset-2">
		<a class="hover:underline" href={links.docsLink}>Docs</a>
		<a class="hover:underline" href={links.supportLink} target="_blank">Support</a>
		<a class="hover:underline" href={links.inviteLink} target="_blank">Invite</a>
		<a class="hover:underline" href="/dash">Dashboard</a>
		<a class="hover:underline" href="/terms">Terms</a>
	</div>
</footer>