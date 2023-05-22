<script>
    let name = 'world';
    let size = 30;
    let editable = false;
    let favorite = '조슈아';

    let where = "";
    let menu = ['커피', '주스', '샌드위치', '김밥'];
    let chosen = [];
    let order = ""; //주문 내용 저장할 변수
    $: order = chosen.length>0 ? `<b>${chosen}</b> 메뉴를 <b>${where=="매장"? "매장 식사를":"포장 주문을"} </b> 선택하셨습니다` : "메뉴를 선택해주세요"
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

    <h1>다중 객체 바인딩</h1>
    <h2>포장: {where}</h2>
    <input type="radio" bind:group={where} value="포장"> 포장합니다
    <input type="radio" bind:group={where} value="매장"> 매장에서 먹을래요

    <h2>메뉴: {chosen}</h2>
    {#each menu as item} 
    <label>
        <input type="checkbox" bind:group={chosen} value={item}> {item}
    </label>
    {/each}
    
    <p>{@html order}</p>
</main>

