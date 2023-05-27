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

    onDestroy(()=> {
        console.log("Child onDestroy 호출됨")
    })

    beforeUpdate(()=> {
        console.log("Child beforeUpdate 호출됨", x)

    })

    afterUpdate(()=> {
        console.log("Child afterUpdate 호출됨", x)
    })

    let x = 0; 
</script>

<h1>Child</h1>
<input type="text" id="text01" bind:value={x}>
<button on:click={()=> {
    x += 1;
}}></button>