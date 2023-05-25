<script>
    // 외부 바인딩
    export let list_todos = [];
</script>

<ul>
    {#each list_todos as item}
    <li>{item}</li>
    {/each}
</ul>