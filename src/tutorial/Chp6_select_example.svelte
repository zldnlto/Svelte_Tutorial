<script>
    let where ='';
    let menu = ['커피', '주스', '샌드위치', '김밥'];
    let chosen = [];
    let order = "";
    $: order = chosen.length >0 ? `<b>${chosen}</b> 메뉴를 <b> ${where == "매장"? "매장 식사를":"포장 주문을"} </b> 선택하셨습니다` : "메뉴를 선택해주세요";

</script>

<main>
    <h2> 포장: {where}</h2>
    <select bind:value={where} name="" id="">
    <option value="">선택하세요</option>
    <option value="포장">포장합니다</option>
    <option value="매장">매장에서 먹을래요</option>
    </select>

    <h2> 메뉴: {chosen}</h2>
    <select multiple bind:value={chosen} name="" id="">
    {#each menu as item}
        <option value={item}>{item}</option>
    {/each}

    <p>{@html order}</p>
</select>
</main>