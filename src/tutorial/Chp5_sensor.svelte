<script>

let count = 0;

//센서 1. 한 줄 구문에 반응형 변수가 있을 떄 
$: console.log("1. 한 줄 구문", count);

//센서 2. 코드 블록 안에 반응형 변수가 있을 때
$: {
    count;
    console.log("2. 코드 블록: count가 변경됨")
}

//센서 3. if 조건에 반응형 변수가 있을 때
$: if(count>0) {
    console.log("3. if조건: count가 0보다 크다.")
}

//센서 4. for loop 안에 반응형 변수가 있을 때 루프 실행
$: for(let i =0; i<4; i++) {
    count;
    console.log("4. for loop 안에 count값 변경됨 for:", i)
}

function addCount(){
    count = count +1; //트리거
}


</script>

<main>
    <button on:click={addCount}>카운트는 {count} 입니다</button>
</main>