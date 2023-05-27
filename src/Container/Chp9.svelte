<script>
  import EventTutorial from "../Chp9/EventTutorial.svelte";
  import SearchButton from "../Chp9/SearchButton.svelte";

let searchText = '';
const customSearch = (event)=> {
    searchText = event.detail.text;
}

</script>


<EventTutorial />

<SearchButton on:searchClicked={customSearch}/>
<br>
{searchText==""?"검색어를 입력 후 Search 버튼을 클릭하세요":"검색어: " + searchText }