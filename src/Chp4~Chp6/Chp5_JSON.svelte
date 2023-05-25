<script>
    let man = {
        age: "10",
        name: {first: "지수", last:"홍"}
    };

    let name = man.name;

    function assignment() {
        man.name.last = "김"
        console.log(name.last);
        // p 태그에 반영하기 위해 동작 감지 필요 
        name = name;
    }
</script>

<main>

    <h2>JSON</h2>
    <p>name.last: {name.last}</p>
    <button on:click={assignment}>할당</button>
</main>