<script>
    import {onMount, beforeUpdate, afterUpdate, onDestroy} from "svelte";


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
<button on:click={()=> x += 1}>add</button>