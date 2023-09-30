<script lang="ts">
	import '../app.css';
	import links from '$lib/links';
	import { base } from '$app/paths';
	import { slide } from 'svelte/transition';
	let innerWidth: number;
	let sideOpen: boolean = true;
</script>

<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@24,400,0,0" />
<svelte:window bind:innerWidth />

<div class="absolute z-50 w-[100%]">
	<nav class="top-0 flex h-10 w-full items-center justify-between gap-5 p-8 text-lg font-bold sm:p-10 sm:text-2xl">
		<a class="bg-gradient-to-br from-indigo-500 from-50% to-sky-500 to-70% bg-clip-text text-transparent" href={base}>LMS</a>

		{#if innerWidth < 426}
			<button
				class="material-symbols-outlined"
				on:click={() => {
					sideOpen = !sideOpen;
				}}
			>
				{sideOpen ? 'collapse_all' : 'expand_all'}
			</button>
		{:else}
			<div class="flex gap-5">
				<a class="hover:underline" href={links.docsLink} target="_blank">Docs</a>
				<a class="hover:underline" href={links.supportLink} target="_blank">Support</a>
				<a class="hover:underline" href={links.inviteLink} target="_blank">Invite</a>
			</div>
		{/if}
		<a class="hover:underline" href="{base}/dash">Login</a>
	</nav>

	{#if sideOpen && innerWidth < 426}
		<div class="flex flex-col border-y-2 border-indigo-600 bg-transparent text-center font-bold text-white backdrop-blur" transition:slide>
			<a class="border-b-2 border-indigo-600 p-4" href={links.docsLink} target="_blank">Docs</a>
			<a class="border-b-2 border-indigo-600 p-4" href={links.supportLink} target="_blank">Support</a>
			<a class="p-4" href={links.inviteLink} target="_blank">Invite</a>
		</div>
	{/if}
</div>

<slot />

<footer class="relative flex flex-col items-center justify-around gap-10 bg-slate-950 p-16 text-lg font-bold md:flex-row">
	<div class="text-center">
		<h1 class="text-8xl">LMS</h1>
		<p>&copy LMS Developer Team</p>
	</div>
	<div class="flex gap-10 underline-offset-2">
		<a class="hover:underline" href={links.docsLink} target="_blank">Docs</a>
		<a class="hover:underline" href={links.supportLink} target="_blank">Support</a>
		<a class="hover:underline" href={links.inviteLink} target="_blank">Invite</a>
		<a class="hover:underline" href="{base}/dash">Dashboard</a>
		<a class="hover:underline" href="{base}/terms">Terms</a>
		<a class="hover:underline" href="{base}/privacy">Privacy</a>
	</div>
</footer>
