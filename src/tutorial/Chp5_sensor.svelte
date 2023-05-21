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

let colors = ['빨강', '주황', '노랑', '초록'];

$: console.log("log.1: ", colors);

function assignment(){
    colors.pop();
    colors = colors;
    console.log("log.2", colors);
}


</script>

<main>
    <button on:click={addCount}>카운트는 {count} 입니다</button>

    <h2>배열은 요소가 할당되면 명시적으로 할당하는 코드가 필요하다</h2>
    <p>colors = colors; 를 꼭 써줘야함</p>
    <p>{colors.join(",")} 모두 {colors.length} 개의 색이 있습니다.</p>
    <button on:click={assignment}>할당</button>
</main>