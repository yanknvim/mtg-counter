<script lang="ts">
	export let rotate = false;
	export let life = 20;

	const increaseLife = () => life += 1;
	const decreaseLife = () => {
		if (life > 0) life -= 1
	};
</script>

<div class="container h-full bg-sky-200 rounded-xl" class:max-md:rotate-180={rotate}>
	<div class="flex h-full items-stretch">
		<button class="flex-1 active:bg-sky-100 text-3xl flex items-center justify-center select-none" on:click={decreaseLife}>
			-
		</button>

		<div class="flex-1 text-center text-6xl font-bold flex items-center justify-center">
			{life}
		</div>

		<button class="flex-1 active:bg-sky-100 text-3xl flex items-center justify-center select-none" on:click={increaseLife}>
			+
		</button>
	</div>
</div>
