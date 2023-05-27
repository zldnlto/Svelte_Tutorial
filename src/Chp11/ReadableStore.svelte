<script>
    import Time from "../Chp11/Time.svelte";
    let flag1 = false;
    let flag2 = false;

    import { elapsed } from './store';
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

    <h1>접속 후 {$elapsed}초가 지났습니다</h1>
</section>