<script lang="ts">
	export let image: string;
	export let title: string;
	export let description: string;
	export let color: string = 'via-fuchsia-500';
</script>

<div class="group relative transition-all duration-500 hover:scale-105">
	<div
		class="absolute -top-0.5 bg-gradient-to-r from-transparent {color} h-full w-full to-transparent opacity-70 transition-all duration-500 group-hover:rounded-3xl group-hover:opacity-100"
	/>
	<div class="relative space-y-5 rounded-2xl border-2 border-slate-800 bg-slate-900 p-10 h-full">
		<div class="flex items-center gap-5">
			<img class="aspect-square w-8 sm:w-16" src={image} alt="" />
			<h1 class="text-lg font-bold sm:text-2xl">{title}</h1>
		</div>
		<p>
			{description}
		</p>
	</div>
</div>
