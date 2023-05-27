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

<!-- 이벤트 제한자 사용하기  -->
<button on:click|once|preventDefault={search}>Search Once ({count})</button>

<div>
    제한자 종류 : preventDefault, stopPropagation, passive, nonpassive, capture, once, self
</div>