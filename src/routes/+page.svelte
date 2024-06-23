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

	<div class="flex gap-3 shrink-0">
		<button class="btn btn-warning" on:click={resetLife}>
			<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M13.5 2c-5.288 0-9.649 3.914-10.377 9h-3.123l4 5.917 4-5.917h-2.847c.711-3.972 4.174-7 8.347-7 4.687 0 8.5 3.813 8.5 8.5s-3.813 8.5-8.5 8.5c-3.015 0-5.662-1.583-7.171-3.957l-1.2 1.775c1.916 2.536 4.948 4.182 8.371 4.182 5.797 0 10.5-4.702 10.5-10.5s-4.703-10.5-10.5-10.5z"/></svg>
		</button>
	</div>

	<Counter bind:life={lifeB} />
</div>

