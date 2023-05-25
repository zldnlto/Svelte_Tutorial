<script>
    //초기 선택, 강제 선택을 위한 변수
    export let choice = '';

    export let list = [
        {code: "apple", desc: "사과"},
        {code: "kiwi", desc: "키위"},
        {code: "mango", desc: "망고"},
        {code: "strawberry", desc: "딸기"},
    ]
</script>


<!-- <main> -->
    <select bind:value={choice}>
        {#each list as item}
        <option value={item.code}>{item.desc}</option>
        {/each}
    </select>
<!-- </main> -->