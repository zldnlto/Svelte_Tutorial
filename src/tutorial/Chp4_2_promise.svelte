<script>
    async function promiseFunc(){
        const result = new Promise((resolve, reject) => {
            setTimeout(()=> {
                // resolve("하이")
                reject(new Error("reject 입니다"))
            
            },3000)
    });
    
    const rtn = await result;
    return rtn;
}

let myPromise = promiseFunc(); //1. 최초 호출하기


</script>
<!-- 2. 버튼 만들어 호출하기 -->
<button on:click={()=> myPromise = promiseFunc()}>async 함수 호출하기</button>

<main>

    <!-- 3. 비동기 함수 결과로 바꾸기 -->
    {#await myPromise}
    <h1>로딩중..</h1>
    {:then res}
    <h1>{res}</h1>
    {:catch error}
    <h1>Error: {error.message}</h1>
    {/await}
</main>

<style></style>