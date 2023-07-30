<script lang="ts">
	export let image: string;
	export let title: string;
	export let description: string;
</script>

<div class="max-w-xl w-80 lg:w-3/4 flex flex-col gap-5 bg-slate-800 p-10 rounded-3xl">
	<div class="flex items-center gap-5">
		<img class="w-16 aspect-square rounded-full justify-self-start" src={image} alt="" />
		<h1 class="text-2xl content-stretch justify-self-start">{title}</h1>
	</div>
	<p class="col-span-2 text-justify">
		{description}
	</p>
</div>
