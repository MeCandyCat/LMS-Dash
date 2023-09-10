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
	<nav class="top-0 flex h-10 w-full items-center justify-between gap-5 p-8 text-lg font-bold sm:p-10 sm:text-2xl">
		<a class="bg-gradient-to-br from-indigo-500 from-50% to-sky-500 to-70% bg-clip-text text-transparent" href={base}>LMS</a>

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
				<a class="hover:underline" href={links.supportLink}>Support</a>
				<a class="hover:underline" href={links.inviteLink}>Invite</a>
			</div>
		{/if}
		<a class="hover:underline" href={base}>Login</a>
	</nav>

	{#if sideOpen && innerWidth < 426}
		<div class=" flex flex-col border-y-2 border-indigo-600 bg-transparent text-center font-bold text-white backdrop-blur" transition:slide>
			<a class="border-b-2 border-indigo-600 p-4" href={links.docsLink}>Docs</a>
			<a class="border-b-2 border-indigo-600 p-4" href={links.supportLink}>Support</a>
			<a class=" p-4" href={links.inviteLink}>Invite</a>
		</div>
	{/if}
</div>

<slot />
