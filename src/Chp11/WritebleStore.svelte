<script>
  import { onDestroy } from 'svelte';

    let rangeValue = 50;

    // 1. store에서 count 임포트 
    import { count } from './store';

    // 2. 구독 ( count 값 변경 시 rangeValue 업데이트하기 )
    const unsubscribe = count.subscribe((v)=> {
        rangeValue = v;
        console.log("변경 감지")
    })

    //3. 구독 종료하기
    onDestroy(unsubscribe);

    //4. 스토어 값 변경하기 (rangeValue값 변경 시 count도 업데이트하기)
</script>


<main>
    <section>
        <h2> count는 {rangeValue} 입니다. </h2>
        <input type="range" bind:value={rangeValue} step=1 min=1 max=100>
    </section>
</main>