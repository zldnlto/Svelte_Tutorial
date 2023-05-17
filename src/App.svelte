<script>
  import Chp4_1 from './tutorial/Chp4_1.svelte';
  import Chp4_2Promise from './tutorial/Chp4_2_promise.svelte';
  import Chp4_3Fetch from './tutorial/Chp4_3_fetch.svelte';
  import Chp4_4Key from './tutorial/Chp4_4_key.svelte';
  import Chp4_5KeyLifecycle from './tutorial/Chp4_5_key_lifecycle.svelte';

  let name = '얄루';
</script>

<main>
  <Chp4_1 name="world" a="{3}" b="{-1}" />
  <Chp4_2Promise />
  <!-- <Chp4_3Fetch/> -->
  <Chp4_4Key />

  <input type="text" bind:value="{name}" />
  {#key name}
    <Chp4_5KeyLifecycle name="{name}" />
  {/key}

  <Chp4_5KeyLifecycle name="{name}" />
</main>

<style>
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
