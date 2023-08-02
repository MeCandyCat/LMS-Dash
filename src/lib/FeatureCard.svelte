<script lang="ts">
	export let image: string;
	export let title: string;
	export let description: string;
	export let color: string = 'via-fuchsia-500';
</script>

<div class="group relative w-64 snap-center transition-all duration-500 hover:scale-105 md:min-w-fit">
	<div
		class="absolute -top-0.5 bg-gradient-to-r from-transparent {color} h-full w-full rounded-2xl to-transparent opacity-60 transition-all duration-500 hover:rounded-3xl group-hover:opacity-100"
	/>
	<div class="relative h-full w-full space-y-5 rounded-2xl bg-slate-900 p-10">
		<div class="flex items-center gap-5">
			<img class="aspect-square w-16 justify-self-start" src={image} alt="" />
			<h1 class="content-stretch justify-self-start text-2xl font-bold">{title}</h1>
		</div>
		<p class="col-span-2 w-96 text-justify">
			{description}
		</p>
	</div>
</div>
