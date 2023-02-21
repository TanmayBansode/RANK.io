<script>
    export let addCountry
</script>

<div id="optionDiv" class="inputdiv" hidden>
    <label class="input">

        <form on:submit={addCountry}>
            <input id="optionEntry" class="input__field" type="text" placeholder="FC Road..." />
            <!-- <span class="input__label">Option Entry</span> -->
          </form>
    </label>
</div>
   

<style>  
      .inputdiv {
        line-height: 1.4;
        font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS",
      sans-serif;
        width: 100%;
        background-color: transparent;
        margin-top: 2%;

      }

      
      
      .input {
        position: relative;
        font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS",
      sans-serif;
      
      }

      .input__field {
        box-sizing: border-box;
        display: block;
        width: 50%;
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

</style>