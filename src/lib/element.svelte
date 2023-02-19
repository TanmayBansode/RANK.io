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
  .name {
    width: 450px;
  }

  .rankcount {
    width: 50px;
    padding: 0;
    text-align: center;
  }

  .element {
    display: flex;
    width: 970px;
    font-family: 'Poppins', sans-serif;
    margin: 8px auto;
    
  }

  .rank {
    width: 75px;
    height: 75px;
    background-color: #08D9D6;
    border-radius: 17px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-right: 5px;
  }
  .main {
    background-color: #393E46;
    margin: auto;
    width: 900px;
    height: 75px;
    border-radius: 17px;
    display: flex;
    padding-left: 20px;
  }

  h1 {
    width: 600px;
    font-size: 2.4rem;
    margin-top: 10px;
    color: white;
    font-family: 'Poppins', sans-serif;
    padding: 0;
    margin-right: 0;
  }

  h2 {
    font-size: 2.5rem;
    color: aliceblue;
    margin: 0;
  }

  h3 {
    color: aliceblue;
    margin: auto;
    font-size: 2.8rem;
    font-weight: lighter;
  }

  .options {
    display: flex;
    margin: 4px 120px 4px 10px;
    padding-left: 120px;
    width: 80px;
    position: relative;
    left: 50px;
  }

  .name {
    display: inline-block;
  }

  .vote {
    width: 60px;
    height: 60px;
    margin: 4px 16px 4px 10px;
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
