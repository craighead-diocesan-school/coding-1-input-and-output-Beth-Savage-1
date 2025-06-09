<script>
  import Header from "$lib/Header.svelte";
  import BulmaExamples from "$lib/BulmaExamples.svelte";
  import ImageCard from "$lib/ImageCard.svelte";
  import HiButton from "../lib/HiButton.svelte";
  import CurrencyConverter from "../lib/CurrencyConverter.svelte";
  let name = "";
  let imageUrl = "https://picsum.photos/200";
  let isChecked = false;
  let selectedOption = "Option 1";
  let count = 0;
  function increment() {
    count = count + 1;
  }
  function decrement() {
    count = count - 1;
  }
</script>

<Header />

<main class="content section">
  <div class="box">
    <h1>Hello {name}!</h1>
    <input bind:value={name} placeholder="Enter your name" />
  </div>
  <div class="box">
    <input type="checkbox" bind:checked={isChecked} />
    <p>The checkbox is {isChecked}.</p>
  </div>
  <div class="box">
    <select bind:value={selectedOption}>
      <option value="Option 1">Option 1</option>
      <option value="Option 2">Option 2</option>
      <option value="Option 3">Option 3</option>
    </select>
    <p>You selected: {selectedOption}</p>
  </div>
  <div class="box">
    <p>Count: {count}</p>
    <button on:click={increment}>+Click</button>
    <button on:click={decrement}>-Click</button>
  </div>
  <HiButton />
  <CurrencyConverter />

  <p>
    Welcome to coding with SvelteKit, a modern JavaScript framework that makes
    it easy to code great apps.
  </p>

  <p>
    This template comes loaded with the <a
      href="https://bulma.io/documentation/">Bulma CSS framework</a
    >, so you can save time and focus on your project.
  </p>
  <img src={imageUrl} alt="Example " />
  <p>
    Here's some examples of colour helpers. You can change the colours in <code
      >theme.scss</code
    >
  </p>
  <BulmaExamples />
  <ImageCard />
</main>

<footer class="footer">
  <p class="has-text-centered">&copy; Craighead Diocesan School 2025</p>
</footer>
