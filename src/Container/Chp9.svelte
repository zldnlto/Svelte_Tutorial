<script>
  import Content from "../Chp9/Content.svelte";
  import EventTutorial from "../Chp9/EventTutorial.svelte";
  import SearchButton from "../Chp9/SearchButton.svelte";
  import SimpleButton from "../Chp9/SimpleButton.svelte";

let searchText = '';
const customSearch = (event)=> {
    searchText = event.detail.text;
}

const simple = (event)=> {
    alert("simple~!")
}
</script>


<EventTutorial />

<SearchButton on:searchClicked={customSearch}/>
<br>
{searchText==""?"검색어를 입력 후 Search 버튼을 클릭하세요":"검색어: " + searchText }

<!-- 이벤트 포워딩 -->
<p>
    <Content on:searchClicked={customSearch}/>
    <br><br>{searchText==""?"검색어를 입력 후 Search 버튼을 클릭하세요":"검색어: " + searchText }
</p>

<!-- 돔 포워딩 -->
<p>
    <SimpleButton on:click={simple}/>
</p>
