<script lang="ts">
	import '../app.css';
	import { base } from '$app/paths';
	import links from '$lib/links';
	import { slide } from 'svelte/transition';

	let innerWidth: number;
	let sideOpen: boolean = true;
</script>

<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@24,400,0,0" />
<svelte:window bind:innerWidth />

<div class="absolute w-[100%] z-50">
	<nav class="top-0 flex items-center justify-between w-full h-10 gap-5 p-8 text-lg font-bold sm:p-10 sm:text-2xl">
		<a class="bg-gradient-to-br from-indigo-500 from-50% to-sky-500 to-70% bg-clip-text text-transparent" href="/">LMS</a>

		{#if innerWidth < 426}
			<button
				class="material-symbols-outlined"
				on:click={() => {
					sideOpen = !sideOpen;
				}}
			>
				{sideOpen ? "collapse_all" : "expand_all"}
			</button>
		{:else}
			<div class="flex gap-5">
				<a class="hover:underline" href={links.docsLink}>Docs</a>
				<a class="hover:underline" href={links.supportLink} target="_blank">Support</a>
				<a class="hover:underline" href={links.inviteLink} target="_blank">Invite</a>
			</div>
		{/if}
		<a class="hover:underline" href="/dash">Login</a>
	</nav>

	{#if sideOpen && innerWidth < 426}
		<div class="flex flex-col font-bold text-center text-white bg-transparent border-indigo-600 border-y-2 backdrop-blur" transition:slide>
			<a class="p-4 border-b-2 border-indigo-600" href={links.docsLink}>Docs</a>
			<a class="p-4 border-b-2 border-indigo-600" href={links.supportLink} target="_blank">Support</a>
			<a class="p-4 " href={links.inviteLink} target="_blank">Invite</a>
		</div>
	{/if}
</div>

<slot />
