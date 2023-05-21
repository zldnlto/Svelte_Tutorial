<script>
  let count = 10;

  $: console.log(`count는 ${count}입니다.`);

  function addCount() {
    count = count + 1;  //트리거
  }
</script>

<p>센서 생성과 동작 정의</p>
<p>
  $: (센서) 뒤에 코드가 위치하는 데 이 코드 안에 반응형 변수(count)가 포함된
  실행 코드가 있어야 합니다.
</p>
<button on:click={addCount}>카운트는 {count}입니다</button>