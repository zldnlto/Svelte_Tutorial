<script>
  import FromChp4To6 from "./Container/FromChp4To6.svelte";
  import Chp8 from "./Container/Chp8.svelte";
  import Chp9 from "./Container/Chp9.svelte";
  import Chp10 from "./Container/Chp10.svelte";
  import Chp11 from "./Container/Chp11.svelte";
  
  let name = '얄루';
</script>

<main>
  <!-- <FromChp4To6/> -->
  <!-- <Chp8/> -->
  <!-- <Chp9 /> -->
  <!-- <Chp10 /> -->
  <Chp11 />
</main>

<style>
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
