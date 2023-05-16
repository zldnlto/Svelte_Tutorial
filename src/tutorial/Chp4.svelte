<script>
	export let name = 'universe';
	export let a = 2;
	export let b = 0;
</script>

<main>
	{#if a>0}
	<h1>Hello {name}!</h1>
	{/if}


	<input type="number" bind:value={b}>
	{#if b === 0}
	<p>{b}입니다</p>
	{:else if b>0}
		<p>{b}은(는) 양수입니다</p>
	{:else}
	<p>{b}은(는) 음수입니다</p>
	{/if}
</main>

<style>

</style>