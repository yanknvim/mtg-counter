<script lang="ts">
	export let rotate = false;
	export let life = 20;

	const increaseLife = () => life += 1;
	const decreaseLife = () => life -= 1;
</script>

<div class="container h-full bg-teal-400 text-accent-content rounded-xl" class:max-md:rotate-180={rotate}>
	<div class="flex h-full">
		<button class="flex-1 active:bg-teal-200 text-3xl flex items-center justify-center rounded-l-xl" on:click={decreaseLife}>
			-
		</button>

		<span class="flex-1 text-6xl font-bold flex items-center justify-center">
			{life}
		</span>

		<button class="flex-1 active:bg-teal-200 text-3xl flex items-center justify-center rounded-r-xl" on:click={increaseLife}>
			+
		</button>
	</div>
</div>
