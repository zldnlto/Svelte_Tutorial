<script>
  import CustomSelect from "../Chp8/CustomSelect.svelte";

  let fruit = "apple";

  let color = "yellow";
  let colorList = [
    {code: "red", desc: "빨강"},
        {code: "yellow", desc: "노랑"},
        {code: "green", desc: "초록"},
        {code: "orange", desc: "주황"},
  ]

  let param = {
    choice: "yellow",
    list: [
      {code: "red", desc: "빨강"},
        {code: "yellow", desc: "노랑"},
        {code: "green", desc: "초록"},
        {code: "orange", desc: "주황"},
    ]
  }

  console.log({...param})
</script>

<ul>
  <li>개발자 A: <CustomSelect /></li>
  <li>개발자 B: <CustomSelect bind:choice={fruit} /> - {fruit} 선택됨</li>
  <li>개발자 C: <CustomSelect list={colorList} bind:color={color} /> - {color} 선택됨 </li>
  <li>spread: <CustomSelect {...param}/>{param.choice} 선택됨</li>
</ul>

<p>객체의 key들과 props가 일치하면 spread를 이용하여 표현할 수 있음</p>
<p>하지만 양방향 바인딩은 되지 않음 (param.choice에 반영되지 않는 것으로 확인)</p>