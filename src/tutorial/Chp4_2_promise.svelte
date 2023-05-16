<script>
    async function promiseFunc(){
        const result = new Promise((resolve, reject) => {
            setTimeout(()=> {resolve("하이")},3000)
    });
    
    const rtn = await result;
    return rtn;
}


</script>

<main>
    {#await promiseFunc()}
    <h1>로딩중..</h1>
    {:then res}
    <h1>{res}</h1>
    {:catch error}
    <h1>Error: {error.message}</h1>
    {/await}
</main>

<style></style>