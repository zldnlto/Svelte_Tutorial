<script>
  import Chp4_1 from '../Chp4~Chp6/Chp4_1.svelte';
  import Chp4_2Promise from '../Chp4~Chp6/Chp4_2_promise.svelte';
  import Chp4_3Fetch from '../Chp4~Chp6/Chp4_3_fetch.svelte';
  import Chp4_4Key from '../Chp4~Chp6/Chp4_4_key.svelte';
  import Chp4_5KeyLifecycle from '../Chp4~Chp6/Chp4_5_key_lifecycle.svelte';
  import Chp4_6Html from '../Chp4~Chp6/Chp4_6_html.svelte';
  import Chp5 from '../Chp4~Chp6/Chp5.svelte';
  import Chp5Json from '../Chp4~Chp6/Chp5_JSON.svelte';
  import Chp5Sensor from '../Chp4~Chp6/Chp5_sensor.svelte';
  import Chp6 from '../Chp4~Chp6/Chp6.svelte';
  import Chp6Each from '../Chp4~Chp6/Chp6_each.svelte';
  import Chp6Contenteditable from '../Chp4~Chp6/Chp6_contenteditable.svelte';
  import Chp6Select from '../Chp4~Chp6/Chp6_select.svelte';
  import Chp6SelectExample from '../Chp4~Chp6/Chp6_select_example.svelte';
  import Chp6Size from '../Chp4~Chp6/Chp6_size.svelte';
  import Chp6This from '../Chp4~Chp6/Chp6_this.svelte';

  let name = '얄루';
</script>

  <Chp4_1 name="world" a="{3}" b="{-1}" />
  <Chp4_2Promise />
  <!-- <Chp4_3Fetch/> -->
  <Chp4_4Key />
  
  <input type="text" bind:value="{name}" />
  {#key name}
    <Chp4_5KeyLifecycle name="{name}" />
  {/key}
  
  <Chp4_5KeyLifecycle name="{name}" />
  <Chp4_6Html />
  <Chp5Sensor />
  <Chp5Json />
  <Chp6 />
  <Chp6SelectExample/>
  <Chp6Contenteditable />
  <Chp6Each />
  <Chp6Size />
  <Chp6This />
