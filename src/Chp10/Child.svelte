<script>
    import {onMount, beforeUpdate, afterUpdate, onDestroy} from "svelte";


    onMount(()=> {
        console.log("Child onMount 호출됨"); 
        document.getElementById("text01").focus();

    })
</script>

<h1>Child</h1>
<input type="text" id="text01">