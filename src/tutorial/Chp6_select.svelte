<script>

let choice = '';
let chosen = [];
</script>

<main>
<p>단일 선택 바인딩</p>
<select bind:value={choice} name="" id="">
<option value="값1">값1 선택</option>
<option value="값2">값2 선택</option>
<option value="값3">값3 선택</option>
</select>

<p>다중 선택 바인딩</p>
<select multiple bind:value={chosen} name="" id="">
    <option value="값1">값1 선택</option>
    <option value="값2">값2 선택</option>
    <option value="값3">값3 선택</option>
    </select>
</main>


<style>

</style>