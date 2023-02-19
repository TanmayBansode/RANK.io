<script>
    export let addCountry
</script>

<div id="optionDiv" class="inputdiv" hidden>
    <label class="input">

        <form on:submit={addCountry}>
            <input id="optionEntry" class="input__field" type="text" placeholder="FC Road..." />
            <span class="input__label">Option Entry</span>
          </form>
    </label>
</div>
   

<style>  
      .inputdiv {
        line-height: 1.4;
        font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS",
      sans-serif;
        margin: 40px auto;
        width: 600px;
        background-color: transparent;

        position: relative;
        bottom: 30px;
      }
      
      .input {
        position: relative;
        font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS",
      sans-serif;
      
      }
      .input__label {
        position: absolute;
        left: 18px;
        top: 12px;
        padding: 0.2rem 0.28rem;
        background: white;
        transition: transform 120ms ease-in;
        font-weight: bold;
        line-height: 1.4;
        font-size: 1.4rem;
        border-radius: 20px;
        font-family: 'Poppins', sans-serif;
      
      }
      .input__field {
        box-sizing: border-box;
        display: block;
        width: 600px;
        padding: 16px;
        color: #393E46;
        background: white;
        border-radius: 25px;
        margin: auto;
        font-size: 1.4rem;
        font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS",
      sans-serif;
      outline: none;
      }
      .input__field:focus + .input__label, .input__field:not(:placeholder-shown) + .input__label {
        transform: translate(0.2rem, -80%) scale(0.8);
        color: #00ADB5;
        background: white;
        padding: 0.2rem 0.5rem;
      }
</style>