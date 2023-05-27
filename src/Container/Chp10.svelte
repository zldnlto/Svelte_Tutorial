<script>
  import Child from "../Chp10/Child.svelte";
  let flag = false;

    
</script>

<section>
    <button on:click={()=> flag = !flag}>{flag == true? "Destroy Child!" : "Create Child!"}</button>

    <p>
        {#if flag}
            <Child />
        {/if}
    </p>
</section>

