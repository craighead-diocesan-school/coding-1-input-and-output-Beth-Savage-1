<script>
  let welcomeMessage = "";
  function sayHi() {
    welcomeMessage = "Hello";
  }
  function resetMessage() {
    welcomeMessage = "";
  }
</script>

<div class="box">
  <button on:click={sayHi}>{welcomeMessage}</button>
  <button class="reset" on:click={resetMessage}>Reset</button>
</div>

<style>
  button {
    width: 5rem;
    height: 5rem;
    margin: 1rem 1rem;
    border: 1px solid #ccc;
    border-radius: 50px;
  }
  button:hover {
    background-color: #f0f0f0;
  }
  .reset {
    width: 2rem;
    height: 2rem;
    margin: 0.5rem 0.5rem;
    border: 1px solid #ccc;
    border-radius: 50px;
    font-size: 0.6rem;
  }
  .box {
    display: flex;
    flex-direction: rows;
  }
</style>
