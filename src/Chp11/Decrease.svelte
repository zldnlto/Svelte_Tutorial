<script>
    import { onDestroy } from "svelte";
    import { count } from "./store";

    let disabled = false;
    $:disabled = $count<=1 ? true : false;
  </script>
  
  <button {disabled} on:click={$count = $count - 1}>count 감소</button>