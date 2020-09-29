<script>
  import Typeform from "svelte-typeform-embed";
  let typeformPopup;

  function openPopup() {
    return typeformPopup.open();
  }

  let value = 100;
</script>

<style>
  main {
    padding: 1em;
    max-width: 320px;
    margin: 0 auto;
    text-align: center;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 2em;
    font-weight: 100;
    margin: 10px 0;
  }

  @media (min-width: 640px) {
    h1 {
      font-size: 4em;
    }
    main {
      max-width: 1140px;
    }
  }

  .wrapper {
    position: relative;
    height: 450px;
    margin-bottom: 45px;
  }

  .hidden {
    position: relative;
  }

  button {
    border: none;
    background-color: #ff3e00;
    padding: 16px 25px;
    border-radius: 4px;
    color: white;
    display: block;
    margin: 0 auto;
  }

  button:hover {
    background-color: #a52a01;
  }
</style>

<main>
  <h1>Svelte Typeform Embed</h1>
  <p>
    A Svelte wrapper component for
    <a href="https://developer.typeform.com/embed/" target="_blank">Typeform
      Embed SDK.</a>
  </p>
  <p>
    Visit
    <strong>
      <a
        href="https://github.com/silvestrevivo/svelte-typeform-embed#readme"
        target="_blank">Github</a></strong>
    or
    <strong>
      <a
        href="https://www.npmjs.com/package/svelte-typeform-embed"
        target="_blank">npm</a></strong>
    for more information
  </p>

  <div class="wrapper">
    <Typeform url="https://showroom.typeform.com/to/ITPUqM" />
  </div>

  <div class="hidden">
    <Typeform
      url="https://showroom.typeform.com/to/ITPUqM"
      bind:typeformPopup
      popup
      autoOpen={false} />
  </div>

  <button on:click={openPopup}>Click to open in popup mode</button>
</main>
