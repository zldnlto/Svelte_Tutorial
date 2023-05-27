<script>
    import {tick, onMount, beforeUpdate, afterUpdate, onDestroy} from "svelte";


    onMount(()=> {
        console.log("Child onMount 호출됨"); 
        document.getElementById("text01").focus();
        
        //onDestroy
        return() => {
            console.log("Child가 파괴되었습니다.")
        }
    })

    beforeUpdate (()=> {
        console.log("Child beforeUpdate 호출됨")
    })

    afterUpdate (()=> {
        console.log("Child afterUpdate 호출됨")
    })

    onDestroy(()=> {
        console.log("Child onDestroy 호출됨")
    })

    let x = 0;

</script>

<h1>Child</h1>
<input type="text" id="text01" bind:value={x}>
<p></p>
<button on:click={async()=> {
        x += 1;
        await  tick(); // tick 호출, DOM 업데이트 기다리기
        console.log("* x값" + x);
        console.log("* DOM" + document.getElementById("text01").value)
    }
}>add</button>