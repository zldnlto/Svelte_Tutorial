<script>
  import Chp8 from "./Container/Chp8.svelte";
import FromChp4To6 from "./Container/FromChp4To6.svelte";
  let name = '얄루';
</script>

<main>
  <!-- <FromChp4To6/> -->
  <Chp8/>
</main>

<style>
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
