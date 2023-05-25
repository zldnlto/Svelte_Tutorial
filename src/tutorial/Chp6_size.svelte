<script>
    let w =500;
    let h = 500;
    let text = "크기 값 바인딩 예제"
    let size = 15;
</script>

<p>{w}px x {h}px</p>

<input type="range" bind:value={size}>

<div bind:clientWidth={w} bind:clientHeight={h}>
    <span style="font-size: {size}px">{text}</span>
</div>

<span>크기 값 바인딩은 오버헤드가 발생할 수 있어 사용하지 않을 것 권고</span>


<style>
    div {
        border: solid gray 1px;
    }
</style>