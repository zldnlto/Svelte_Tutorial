<script>
  export let name = 'universe';
  export let a = 2;
  export let b = 0;

  let colors = ['빨강', '노랑', '파랑', '보라'];

  let emailCard = { _id: 'a1', name: '둘리', email: 'd2@mail.com', age: 10 };

  console.log(Object.entries(emailCard));
</script>

<main>
  {#if a > 0}
    <h1>Hello {name}!</h1>
  {/if}

  <input type="number" bind:value="{b}" />
  {#if b === 0}
    <p>{b}입니다</p>
  {:else if b > 0}
    <p>{b}은(는) 양수입니다</p>
  {:else}
    <p>{b}은(는) 음수입니다</p>
  {/if}

  <!-- each 루프문  -->
  <ul>
    {#each colors as color}
      <li>{color}</li>
    {/each}
  </ul>
  <!-- each 루프문 안에서 index 사용하기 -->
  <ul>
    {#each colors as color, idx}
      <li>{idx + 1} : {color}</li>
    {/each}
  </ul>
  <!-- select로 응용하기  -->
  <select name="" id="">
    <option value="">선택하세요</option>
    {#each colors as color, idx}
      <option> {idx + 1}: {color}</option>
    {/each}
  </select>

  <!-- JSON 객체 다루기 - JSON을 배열 형태로 만든 후 사용 -->
  {#each Object.entries(emailCard) as [key, value], idx}
    <p>{idx}번째 키: {key}의 값은 {value}</p>
  {/each}
</main>

<style>
</style>
