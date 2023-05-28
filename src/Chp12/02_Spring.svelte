<script>
    import { spring } from 'svelte/motion';

    let coords = spring({x: 50, y:50}, {
        stiffness: 0.1, // 따라오는 속도 : 느림 0 <> 1 빠름 
        damping: 0.5, // 멀어지는 거리 : 넓음 0 <> 1 좁음
        precision: 0.3, // 튕겨지는 횟수 : 많음 0 <> 적음
    })
    //원의 지름값과 바인딩할 스토어 생성 
    let size = spring(10);
    coords.subscribe (v=> console.log(v.x, v.y))

</script>

<p>
    stiffness : 스토어에 설정한 값까지 도달하는 속도 (1에 가까울수록 빠르게 도달)
</p>
<p>
    damping : 스토어에 설정한 값을 초과했다가 다시 돌아오는 옵션
</p>
<p>
    precision : 스토어에 설정한 값을 초과하는 횟수. (damping의 튕김 횟수)
</p>

<svg on:mousemove="{e=> coords.set({x: e.clientX, y:e.clientY})}" on:mousedown="{()=> size.set(30)}" on:mouseup="{()=> size.set(10)}">
    <circle cx={$coords.x} cy={$coords.y} r={$size}/>
</svg>

<style>
    svg {
        width: 100%;
        height: 100%;
        margin: -8px;
    }
    
    circle {
        fill: #080808;
    }

</style>