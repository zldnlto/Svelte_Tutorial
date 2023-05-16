<script>
	import Chp4 from './tutorial/Chp4.svelte'
</script>

<main>
	<Chp4 name="world" a={3} b={-1}/>
</main>

<style>

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>