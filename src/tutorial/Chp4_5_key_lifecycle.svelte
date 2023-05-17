<script>
  import { afterUpdate, beforeUpdate, onDestroy, onMount } from 'svelte';

  onMount(() => console.log('Component 생성됨'));
  onDestroy(() => console.log('Component 파괴됨'));

  export let name;
  //   상위 컴포넌트로부터 값을 주입받기 위해 설정
</script>

<p>hello {name}!</p>
