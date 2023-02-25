<script>
  export let rank;
  export let country;
  export let upvote;
  export let downvote;
</script>

<div class="element">
  <div class="rank">
    <h2>
      #{rank}
    </h2>
  </div>
  <div class="main">
    <div class="name">
      <h1>
        {country.name}
      </h1>
    </div>
    <div class="options">
      <button on:click={upvote(country)} class="upvote vote">
        <img src="https://user-images.githubusercontent.com/113820623/219949607-e111d6ec-6efd-47e0-bd4c-163128325e58.png" alt="" class="imgu" />
      </button>

      <button on:click={downvote(country)} class="downvote vote">
        <img src="https://user-images.githubusercontent.com/113820623/219949607-e111d6ec-6efd-47e0-bd4c-163128325e58.png" alt="" class="imgd" />
      </button>

    </div>

    <div class="rankcount">
      <h3>
        {country.votes}
      </h3>
    </div>
  </div>
</div>

<style>
 


  .element {
    display: flex;
    width: 100%;
    font-family: 'Poppins', sans-serif;
    margin: 8px auto;
    
  }

  .rank {
    width: 8%;
    height: 75px;
    background-color: #08D9D6;
    border-radius: 17px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .main {
    background-color: #393E46;
    margin: auto;
    width: 90%;
 height: 75px;
    border-radius: 17px;
    display: flex;

  }

  h1 {
    width: 100%;
    font-size: 2.4rem;
    margin: 1.3% 3%;
    color: white;
    font-family: 'Poppins', sans-serif;
    padding: 0;

  }

  h2 {
    font-size: 2.3rem;
    color: aliceblue;
    margin: 0;
    width: auto;
  }

  h3 {
    color: aliceblue;
    margin: auto;
    font-size: 2.8rem;
    font-weight: lighter;
  }

   .name {
    width: 70%;
  }

  .options {
    display: flex;
    margin: 4px 0;
    width: 18%;
  }

    .rankcount {
    width: 6%;
    margin: auto;
    text-align: center;
  }


  .vote {
    width: 10%;
    height: 60px;
    margin: 4px auto;
    background: none;
	  color: inherit;
	  border: none;
	  padding: 0;
	  font: inherit;
	  cursor: pointer;
	  outline: inherit;
  }

  .imgu {
    width: 40px;
    transform: rotate(-90deg) scale(1.5);
    margin: auto;
  }

  .imgd {
    width: 40px;
    transform: rotate(90deg) scale(1.5);
    margin: auto;
  }
</style>
