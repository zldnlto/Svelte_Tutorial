<script>
	import Chp4 from './tutorial/Chp4.svelte'
  import Chp4_2Promise from './tutorial/Chp4_2_promise.svelte';
  import Chp4_3Fetch from './tutorial/Chp4_3_fetch.svelte';
</script>

<main>
	<Chp4 name="world" a={3} b={-1}/>
	<Chp4_2Promise />
	<Chp4_3Fetch/>
</main>

<style>

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>