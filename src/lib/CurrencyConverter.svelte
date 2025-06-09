<script>
  let USD = 1.0;
  let NZD = 1.66;
  function convertCurrency() {
    NZD = USD * 1.66;
  }
</script>

<div class="box">
  <p>Convert currency</p>
  <input bind:value={USD} placeholder="Enter amount" />
  <button on:click={convertCurrency}>Convert to NZD</button>
  <p>{USD} USD is approximately {NZD} NZD</p>
</div>

<style>
  button {
    margin-top: 1rem;
    padding: 0.5rem 1rem;
    background-color: #3273dc;
    color: white;
    border-radius: 20%;
  }
</style>
