<script>
    let name = 'world';
    let size = 30;
    let editable = false;
    let favorite = '조슈아';
</script>

<main>
    <!-- 스크립트 변수 name과 HTML input의 양방향 바인딩 -->
    <input type="text" bind:value={name}>
    <h1>Hello {name}!</h1>
    <p>input 엘리먼트의 value가 name을 변화시킴 (뷰->데이터)</p>
    <p>name을 출력한 h1 엘리먼트 텍스트가 자동으로 업데이트(데이터-> 뷰)</p>

    <input type="range" bind:value={size} min=0 max=100> <br/>
    <input type="number" bind:value={size}>

    <h1 style="font-size:{size}px">폰트 사이즈 조정해봐용 {name}</h1>

    <input type="checkbox" bind:checked={editable}> 수정 체크
    {#if editable}
    <p>수정 모드 : <input type="text" bind:value={favorite}></p>
    {:else}
    <p>보기 모드 : {favorite}</p>
    {/if}
</main>

