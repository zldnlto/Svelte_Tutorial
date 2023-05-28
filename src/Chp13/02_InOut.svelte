<script>
    import { fade , fly } from 'svelte/transition'
    let visible = true;
</script>


<label>
    <input type="checkbox" bind:checked={visible}>
    visible
</label>

{#if visible}
    <p in:fly="{{y: 200, duration: 2000}}" out:fade>
    아래서 날아 들어오고, 조용히 사라져라!
    </p>

{/if}