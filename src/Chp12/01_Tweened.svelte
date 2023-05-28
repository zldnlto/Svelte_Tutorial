<script>
    import {tweened} from 'svelte/motion';
    import {cubicIn} from 'svelte/easing';

    const progress = tweened(0, {
        duration: 1000,
    });

    const progress2 = tweened(0, {
        duration: 1000,
        easing: cubicIn
    })

    progress.subscribe(v => console.log(v))
</script>


<p>duration - 현재 값을 조금씩 증가 또는 감소시켜 1000ms 안에 1이 될 때까지 업데이트</p>

<p> 스토어에 어떤 값을 지정하면 1000ms의 시간동안 점진적으로 증가하여 지정한 값에 도달하라는 설정</p>
<p>스토어와 똑같이 사용했지만 내부에서는 여러 번 값을 변경해준다</p>

<a href="https://svelte.dev/docs#svelte_easing">easing 참고</a>

<progress value={$progress}></progress>
<progress value={$progress2}></progress>
<button on:click="{()=> {$progress = 0; $progress2 = 0}}">0%</button>
<button on:click="{()=> {progress.set(0.5); progress2.set(0.5)}}">50%</button>
<button on:click="{()=> {progress.set(1); progress2.set(1)}}">100%</button>


<style>
    progress { width: 100% }
</style>