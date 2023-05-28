<script>
    import { fade } from 'svelte/transition'

    let grandparent = true;
    let parent = true;
</script>

<p>
    <input type="checkbox" bind:checked={grandparent}>할아버지, 할머니
</p>
<p>
    <input type="checkbox" bind:checked={parent}>부모님
</p>

{#if grandparent} 
    {#if parent}
        <p transition:fade> 형 - 어른 말씀 잘 들음</p>
        <p transition:fade|local> 동생 - 부모님 말만 잘 듣는 local </p>
    {/if}


{/if}