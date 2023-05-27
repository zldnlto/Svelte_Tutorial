<script>
    import Time from "../Chp11/Time.svelte";
    let flag1 = false;
    let flag2 = false;
</script>

<section>
    <input type="checkbox" bind:checked="{flag1}"> 시간 표시 1 
    <input type="checkbox" bind:checked="{flag2}"> 시간 표시 2 

    {#if flag1} 
    <Time />
    {/if}

    {#if flag2} 
    <Time />
    {/if}
</section>