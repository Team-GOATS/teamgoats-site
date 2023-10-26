<script>
  import Basic from "svelte-toggles/src/Basic";
  import Eclipse from "svelte-toggles/src/Eclipse";
  import Expand from "svelte-toggles/src/Eclipse";
  import Slide from "svelte-toggles/src/Slide";
</script>

<ul class="toggleContainer">
  <li class="toggleCard">
    <Slide />
    <div class="cardBody">
      <h3>Toggle Switch - Basic</h3>
      <a href="https://github.com/Team-GOATS/svelte-toggles-npm-package"
        >Check More</a
      >
    </div>
  </li>
  <li class="toggleCard">
    <Eclipse />
    <div class="cardBody">
      <h3>Toggle Switch - Eclipse</h3>
      <a href="https://github.com/Team-GOATS/svelte-toggles-npm-package"
        >Check More</a
      >
    </div>
  </li>
  <li class="toggleCard">
    <Expand />
    <div class="cardBody">
      <h3>Toggle Switch - Expand</h3>
      <a href="https://github.com/Team-GOATS/svelte-toggles-npm-package"
        >Check More</a
      >
    </div>
  </li>
  <li class="toggleCard">
    <Slide />
    <div class="cardBody">
      <h3>Toggle Switch - Slide</h3>
      <a href="https://github.com/Team-GOATS/svelte-toggles-npm-package"
        >Check More</a
      >
    </div>
  </li>
</ul>

<style>
  .toggleContainer {
    display: grid;
    grid-template-columns: 1fr;
    row-gap: 20px;
    column-gap: 30px;
    margin: 20px;
  }

  .toggleCard {
    list-style: none;
    display: flex;
    flex-direction: column;
    border-radius: 10px;
    overflow: hidden;
  }

  .cardBody {
    display: flex;
    flex-direction: column;
    padding: 15px;
  }

  .cardBody a {
    color: #4a90e2;
    font-weight: 600;
  }

  .cardBody a:hover {
    color: #235dab;
    text-decoration: underline;
  }

  @media (min-width: 768px) {
    .toggleContainer {
      grid-template-columns: 1fr 1fr;
      gap: 0;
    }
  }

  @media (min-width: 980px) {
    .toggleContainer {
      grid-template-columns: 1fr 1fr 1fr 1fr;
      gap: 25px;
    }
  }
</style>
