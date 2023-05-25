<script>
    let customers = [
        {disable: false, email:"joshua@mail.com", mailType:"home", name:"홍지수", age:29, grade:"gold"},
        {disable: false, email:"boo@mail.com", mailType:"office", name:"부승관", age:25, grade:"silver"},
        {disable: false, email:"hoshi@mail.com", mailType:"home", name:"권순영", age:28, grade:"gold"},
        {disable: false, email:"hong@mail.com", mailType:"home", name:"홍길동", age:26, grade:"normal"},
    ]

</script>

<!-- 데이터를 표로 표현하기 -->

<table border=1>
    <thead>
        <th>탈퇴여부</th>
        <th>이메일</th>
        <th>메일 타입</th>
        <th>이름</th>
        <th>나이</th>
    </thead>
    <tbody>
        {#each customers as cust}
            <tr>
                
                <td>{cust.disable}</td>
                <td><input type="text" bind:value={cust.email} disabled={cust.disable}></td>
                <td> [ 집: <input type="radio" bind:group={cust.mailType} value="home" disabled={cust.disable}> | 회사: <input type="radio" bind:group={cust.mailType} value="office" disabled={cust.disable}> ]</td>
                <td><input type="text" bind:value={cust.name} disabled={cust.disable}></td>
                <td><input type="number" bind:value={cust.age} disabled={cust.disable}></td>
                <td>
                    <select bind:value={cust.grade} >
                        <option value="gold">골드</option>
                        <option value="silver">실버</option>
                        <option value="normal">일반</option>
                    </select>
                </td>
            </tr>
        {/each}
    </tbody>
</table>


<style>
    table {
        width: 100%;
        border: 1px solid;
        border-collapse: collapse; /* table 안쪽 선은 한줄로 표시  */
    }
    
    th, td {
        border: 1px solid;
        padding: 10px;
    }
</style>