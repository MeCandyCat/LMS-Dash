<script lang="ts">
	export let image: string;
	export let title: string;
	export let description: string;
</script>

<div class="relative max-w-xl w-80 lg:w-3/4 group">
	<div
		class="absolute -top-0.5 left-1 bg-gradient-to-r from-transparent from-5% via-fuchsia-500 to-transparent to-95% opacity-75 transition-all duration-500 group-hover:opacity-100 h-[95%] w-[98.5%] rounded-3xl"
	/>
	<div class=" bg-slate-900 relative p-10 space-y-5 rounded-3xl h-full w-full">
		<div class="flex items-center gap-5">
			<img class="w-16 aspect-square rounded-full justify-self-start" src={image} alt="" />
			<h1 class="text-2xl content-stretch justify-self-start">{title}</h1>
		</div>
		<p class="col-span-2 text-justify">
			{description}
		</p>
	</div>
</div>
