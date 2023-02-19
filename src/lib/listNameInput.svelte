<script>
    export let addName

</script>

<div class="inputdiv">
    <label class="input">

        <form on:submit={addName} id="form">
            <input class="input__field" type="text" placeholder="Saturday Lunch Plan" />
            <span class="input__label">Voting for ?</span>
          </form>


    </label>
</div>
   

<style>  
      .inputdiv {
        font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS",
      sans-serif;
        margin: 100px auto;
        width: 500px;
      }
      
      .input {
        position: relative;
        font-family: 'Poppins', sans-serif;
      outline: none;
      }
      .input__label {
        position: absolute;
        left: 18px;
        top: 6px;
        padding: 0.2rem 0.28rem;
        background: white;
        font-weight: bold;
        line-height: 1.4;
        font-size: 2rem;
        border-radius: 25px;
        width: 440px;
        text-align: center;
        color: #393E46;
        font-family: 'Poppins', sans-serif;
      
      }
      .input__field {
        box-sizing: border-box;
        display: block;
        width: 100%;
        padding: 16px;
        color: black;
        background: white;
        border-radius: 25px;
        margin: auto;
        font-size: 1.4rem;
        font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS",
      sans-serif;
      outline: none;
      }
      .input__field:focus + .input__label, .input__field:not(:placeholder-shown) + .input__label {
        transform: translate(0rem, 0%) scale(0);
        background: white;
        z-index: -3;
        padding: 0.2rem 0.5rem;
        width: 50px;

      }
</style>