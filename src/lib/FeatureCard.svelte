<script lang="ts">
	export let image: string;
	export let title: string;
	export let description: string;
	export let color: string = 'via-fuchsia-500';
</script>

<div class="snap-center relative w-64 md:min-w-fit group transition-all duration-500 hover:scale-105">
	<div
		class="absolute -top-0.5 bg-gradient-to-r from-transparent {color} to-transparent opacity-60 transition-all duration-500 group-hover:opacity-100 h-full w-full rounded-2xl hover:rounded-3xl"
	/>
	<div class="bg-slate-900 relative p-10 space-y-5 h-full w-full rounded-2xl">
		<div class="flex items-center gap-5">
			<img class="w-16 aspect-square justify-self-start" src={image} alt="" />
			<h1 class="text-2xl font-bold content-stretch justify-self-start">{title}</h1>
		</div>
		<p class="col-span-2 text-justify w-96">
			{description}
		</p>
	</div>
</div>
