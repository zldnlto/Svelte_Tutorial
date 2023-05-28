<script>
import { fade, blur, fly, slide, scale } from "svelte/transition";

    let show = true;
</script>

<button on:click={()=> show = !show}>Toggle</button>

{#if show} 
    <h1 transition:fade> fade는 점점 사라집니다</h1>
    <h1 transition:blur> blur는 점점 뿌옇게...</h1>
    <h1 transition:fly> fly는 날아다녀요</h1>
    <h1 transition:slide> slide는 커튼처럼</h1>
    <h1 transition:scale> 멀어지며 작아지는</h1>
{/if}