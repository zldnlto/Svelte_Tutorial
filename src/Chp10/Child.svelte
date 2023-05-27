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
</script>

<h1>Child</h1>
<input type="text" id="text01">