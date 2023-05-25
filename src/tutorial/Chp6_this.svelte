<script>
    import { onMount } from "svelte";
    import List from './Chp6_List.svelte'

    onMount(async () => {
        todoInput.focus();
    })

    let todos =[];
    let todoInput;
    let todo = '';

    const add = () => {
        if(todo.replaceAll(" ",'')==""){
            alert("값을 입력하세요");
            todoInput.focus();
        }else{
            todos.push(todo);
            todos = todos;
            todo = '';
            todoInput.focus();
        }
    }
    const remove = () => {
        todos = [];
        todoInput.focus();
    }
</script>

<main>
<p>제어를 위해 객체를 참조해야 할 경우(input박스에 포커스를 주는 경우)</p>

<input type="text" bind:this={todoInput} bind:value={todo}/>
<button on:click={add}>추가</button>

<List list_todos = {todos}/>

<button on:click={remove}>전부 삭제</button>

</main>
