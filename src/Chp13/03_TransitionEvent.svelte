<script>
    import { fly } from "svelte/transition";

    let visible = true;
    let status = "이벤트 기다리는 중 ..";
</script>

<p>이벤트 상태: {status}</p>

<label>
    <input type="checkbox" bind:checked={visible}>
    visible
</label>

{#if visible}
    <p 
        transition:fly="{{y:200, duration: 2000}}"
        on:introstart="{()=> status = '등장 시작'}"
        on:introend="{()=> status = '등장했어요'}"
        on:outrostart="{()=> status = '퇴장 시작'}"
        on:outroend="{()=> status = '퇴장했어요'}">
        트랜지션 이벤트 처리하기
    </p>

{/if}