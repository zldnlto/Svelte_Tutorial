<script>
    let count = 0;
    const search = (event) => {
        console.log("조회 버튼 클릭")
        console.log(event.target)
        count = count +1;
    }
</script>
<button on:click={search}>
Search ({count})
</button>

<button  on:click={(event)=> {
    console.log(event.target);
    count = count +1;
}}>Button Inline ({count})</button>

<style>

</style>