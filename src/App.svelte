<svelte:head>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" >
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@1,800&family=Phudu:wght@500&family=Poppins:wght@200;400&display=swap" rel="stylesheet">
</svelte:head>


<script>
  import List from './lib/list.svelte'
</script>

<main class="main-container">
  <div class="title-div">
    <h1 class="section-title"> RANK.io </h1>
    <h3>A Simple Voting Tool</h3>
  </div>
  <List />
  <hr>
  <h4 class="end-credit">© Tanmay Bansode</h4>
</main>

<style>


.section-title{
  font-size: 4.4rem;
  font-weight: bold;
  color: #fcffe7; 
  font-family: 'Montserrat', sans-serif;


}

.title-div{
 text-align: center;
 padding-top: 50px;
 padding-bottom: 40px;
 background-image: linear-gradient(to right, #3498db, #10d7af, #3498db);
}

h3 {
    color: #f0f1e5f1;
    font-family: 'Poppins', sans-serif;
    font-weight: 500;
    position: relative;
    font-style: italic;
  }

  .end-credit{
  text-align: center;
  margin: 3% auto;
  color: #f0f1e5f1;
  font-family: 'Poppins', sans-serif;
  font-weight: lighter;
  font-style: normal;
}


hr {
    border-top: 3px simple #eeeeee;
    border-bottom: 0;
    align-items: center;
    width: 80%;
    background-color: #222831;
    margin-top: 50%;
  }

</style>
