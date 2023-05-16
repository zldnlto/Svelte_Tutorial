<script>
	let name = 'universe';
	let a = 2;
</script>

<main>
	{#if a>0}
	<h1>Hello {name}!</h1>
	{/if}
</main>

<style>

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>