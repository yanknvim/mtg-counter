<script>
	let lifeA;
	let lifeB;

	const resetLife = () => {
		lifeA = 0;
		lifeB = 0;
	}
</script>

<div class="flex">
	<button on:click={resetLife}>Reset</button>
</div>
