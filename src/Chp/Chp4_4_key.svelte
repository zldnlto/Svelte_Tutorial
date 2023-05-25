<script>
  let name = 'world';
</script>

<main>
  <input type="text" bind:value="{name}" />
  <p>비교용 시각: {Date()}</p>

  {#key name}
    <p>렌더링 시각: {Date()}</p>
    <h1>Hello {name}! 컴포넌트 파괴하고 재생성</h1>
  {/key}
</main>
