<script>
    let count = 0;
    const search = (event) => {
        console.log("조회 버튼 클릭")
        console.log(event.target)
        count = count +1;
    }

    const increase = () => {
        console.log("increase");
        count = count +1;
    }
</script>

<button on:click={search} on:click={increase}>
Search ({count})
</button>

<style>

</style>