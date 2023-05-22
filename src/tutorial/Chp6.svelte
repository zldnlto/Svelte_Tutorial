<script>
    let name = 'world';
</script>

<main>
    <!-- 스크립트 변수 name과 HTML input의 양방향 바인딩 -->
    <input type="text" bind:value={name}>
    <h1>Hello {name}!</h1>
    <p>input 엘리먼트의 value가 name을 변화시킴 (뷰->데이터)</p>
    <p>name을 출력한 h1 엘리먼트 텍스트가 자동으로 업데이트(데이터-> 뷰)</p>
</main>