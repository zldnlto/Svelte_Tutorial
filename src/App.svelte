<script>
  import Chp8 from "./Container/Chp8.svelte";
  import Chp9 from "./Container/Chp9.svelte";
import FromChp4To6 from "./Container/FromChp4To6.svelte";
  let name = '얄루';
</script>

<main>
  <!-- <FromChp4To6/> -->
  <!-- <Chp8/> -->
  <Chp9 />
</main>

<style>
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
