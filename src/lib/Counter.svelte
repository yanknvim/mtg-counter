<script lang="ts">
	export let rotate = false;
	export let life = 20;

	const increaseLife = () => life += 1;
	const decreaseLife = () => {
		if (life > 0) life -= 1
	};
</script>

<div class="container h-full bg-accent text-accent-content rounded-xl" class:max-md:rotate-180={rotate}>
	<div class="flex h-full">
		<button class="flex-1 active:bg-white text-3xl flex items-center justify-center" on:click={decreaseLife}>
			-
		</button>

		<span class="flex-1 text-6xl font-bold flex items-center justify-center">
			{life}
		</span>

		<button class="flex-1 active:bg-white text-3xl flex items-center justify-center" on:click={increaseLife}>
			+
		</button>
	</div>
</div>
