<script>
  import Element from "./element.svelte";
  import Entry from "./entry.svelte";
  import ListNameInput from "./listNameInput.svelte";
  import ListName from "./listName.svelte";
  export let listName;

  const sort = (countriesArray) => {
    countriesArray.sort((a, b) => {
      return b.votes - a.votes;
    });
  };


  const upvote = (country) => {
    country.votes += 1;
    sort(countriesArray);
    countriesArray = [...countriesArray];
  };

  const downvote = (country) => {
    country.votes -= 1;
    sort(countriesArray);
    countriesArray = [...countriesArray];
  };

  const addCountry = (event) => {
    event.preventDefault();
    const input = event.target.querySelector('input[type="text"]');
    const countryName = input.value;
    input.value="";
    countriesArray.push({
      name: countryName,
      votes: 0,
    });
    const box = document.getElementById("listoften");
    box.style.padding = "4px 8px";
    box.style.borderStyle = "solid"

    sort(countriesArray);
    countriesArray = [...countriesArray];
  };

  let countries = [];

  let countriesArray = countries.map((country) => {
    return {
      name: country,
      votes: 0,
    };
  });

  const addName = (event) => {
    event.preventDefault();
    const input = event.target.querySelector('input[type="text"]');
    listName= input.value;
    const form = document.getElementById("form");
    form.style.display = "none";
    const optionDiv = document.getElementById("optionDiv");
    optionDiv.removeAttribute("hidden");
    const optionEntry = document.getElementById("optionEntry");
    optionEntry.focus();
  }

</script>

<main>

    <ListName {listName}/>
    <ListNameInput {addName}/>
  <div id="listoften">

    {#each countriesArray as country, i}
      <Element {country} {upvote} {downvote} rank={i + 1} />
    {/each}
  </div>

  <Entry {addCountry}/>
</main>

<style>
  #listoften {
    background-color: transparent;
    width: 1000px;
    margin: auto;
    border-radius: 15px;
    border-color: rgb(145, 149, 153);

    position: relative;
    bottom: 40px;

  }


</style>
