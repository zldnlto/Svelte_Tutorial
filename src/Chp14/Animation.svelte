<script>
    import { flip } from 'svelte/animate'
    import { quintOut } from 'svelte/easing'; 
    
    let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9];

    function shuffle(){
        numbers = numbers.sort(()=> 0.5 - Math.random());
    }
</script>

<button on:click={shuffle}>섞기</button>
<div>
    {#each numbers as number (number) }
        <button animate:flip={{delay:250, duration:250, easing: quintOut}}>{number}</button>
        
    {/each}
</div>

<p>animate 사용 시 참고</p>

<p>1. 키가 선언되어 있는 #each 블록에서 사용해야 함 - 직전 예제에서 (number) 형태로 키를 선언해야 정상 동작함</p>
<p>2. 배열의 인덱스의 변화가 있어야 동작한다</p>
<p>3. each 바로 아래에 하위 엘리먼트로 선언해야 한다</p>