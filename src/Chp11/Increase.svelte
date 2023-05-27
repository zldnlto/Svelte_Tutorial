<script>
  import { onDestroy } from "svelte";
  import { count } from "./store";
    
    let disabled = false;

    function Increase () {
        count.update((n)=> {
            return n + 1;
        })
    }
    //count 구독 구현, count값이 100보다 클 때 비활성화
    const unsub = count.subscribe((v)=> {
        disabled = v >= 100 ? true : false;
    })

    onDestroy(unsub);
</script>

<button disabled={disabled} on:click={Increase}>count 증가</button>