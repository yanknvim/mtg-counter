<script lang="ts">
	import Counter from "$lib/Counter.svelte";

	let lifeA;
	let lifeB;

	const resetLife = () => {
		lifeA = 20;
		lifeB = 20;
	};
</script>

<div class="flex max-md:flex-col p-5 gap-5 h-dvh items-center">
	<Counter rotate=true  bind:life={lifeA} />
	<button class="shrink-0 bg-gray-100 h-fit w-fit px-3 py-2 rounded-xl" on:click={resetLife}>Reset</button>
	<Counter bind:life={lifeB} />
</div>

