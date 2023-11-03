<script>
  import Header from "./lib/Header.svelte";
  import Footer from "./lib/Footer.svelte";
  import Basic from "./lib/toggles/Basic.svelte";
  import Toggle2 from "./lib/toggles/Toggle2.svelte";
  import Toggle3 from "./lib/toggles/Toggle3.svelte";
</script>

<main>
  <Header />

  <section class="intro-section">
    <h1>Svelte Toggle Switches</h1>

    <p>
      Svelte Toggles Switches - your one-stop shop for Light & Dark mode
      solusion! We've got all the Local Storage mumbo-jumbo covered; all you
      need is your creative touch to switch themes. Svelte Toggles will continue
      to be maintained, ensuring you have reliable support in the long run. So
      why break a sweat when you can switch with a smile? Join the Svelte
      Toggles revolution today!
    </p>

    <a
      href="https://github.com/Team-GOATS/svelte-toggles-npm-package#user-content-get-started"
      >GET STARTED</a
    >
  </section>

  <section class="toggleLists">
    <ul>
      <li>
        <div class="toggle-container basic-container">
          <Basic />
        </div>
        <a href="https://github.com/Team-GOATS/svelte-toggles-npm-package">
          <div class="toggle-info">
            <h3 class="toggle-name">Basic</h3>
            <p class="toggle-description">Sun Morphs into Moon</p>
            <p class="check-more">Check More</p>
          </div>
        </a>
      </li>

      <li class="toggle2">
        <div class="toggle-container commingsoon-container">
          <Toggle2 />
        </div>
        <a href="https://github.com/Team-GOATS/svelte-toggles-npm-package">
          <div class="toggle-info">
            <h3 class="toggle-name">Toggle2</h3>
            <p class="toggle-description">Coming soon ...</p>
            <p class="check-more">Stay tuned!</p>
          </div>
        </a>
      </li>

      <li class="toggle3">
        <div class="toggle-container commingsoon-container">
          <Toggle3 />
        </div>
        <a href="https://github.com/Team-GOATS/svelte-toggles-npm-package">
          <div class="toggle-info">
            <h3 class="toggle-name">Toggle3</h3>
            <p class="toggle-description">Coming soon ...</p>
            <p class="check-more">Stay tuned!</p>
          </div>
        </a>
      </li>
    </ul>
  </section>

  <Footer />
</main>

<style>
  main {
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    gap: 2rem;
    width: 100vw;

    min-height: 100vh;
    margin: 0 auto;
  }

  section {
    margin: 1.5rem auto;
    width: 80%;
    max-width: 1400px;
  }

  /* section1: introduction */
  .intro-section {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 0.7rem;
  }

  .intro-section h1 {
    background: linear-gradient(to right, #2563eb, #3eadcf);
    -webkit-background-clip: text; /* For compatibility with some web browsers */
    background-clip: text;
    color: transparent;
  }

  .intro-section p {
    font-size: 1.2rem;
    line-height: 1.5;
    width: 75%;
    text-align: center;
    margin: 2rem;
  }

  .intro-section a {
    color: #f5f5f5;
    border-radius: 2.5rem;
    background-color: #4a90e2;
    font-size: 1.3rem;
    font-weight: bold;
    padding: 0.6rem 2.2rem;
    transition: all 0.4s ease-in-out;
  }

  .intro-section a:hover {
    background-color: #4570e6;
    text-decoration: underline;
  }

  /* section2: toggle list */
  .toggleLists {
    display: grid;
    justify-items: stretch;
    justify-content: center;
  }

  ul {
    width: 100%;
    display: grid;
    grid-template-columns: repeat(1, minmax(10rem, 20rem));
    grid-template-rows: 1fr;
    row-gap: 3rem;
    column-gap: 2rem;
    justify-items: stretch;
    align-items: stretch;
  }

  li {
    list-style: none;
    border-radius: 0.375rem;
    overflow: hidden;
    transition-property: all;
    transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
    transition-duration: 0.15s;
  }

  li:hover {
    transform: scale(1.05);
  }

  .toggle2,
  .toggle3 {
    display: none;
  }

  @media (min-width: 768px) {
    ul {
      grid-template-columns: repeat(2, minmax(10rem, 20rem));
      gap: 3rem;
    }

    .toggle2 {
      display: block;
    }

    .intro-section p {
      width: 62%;
      max-width: 52rem;
    }
  }

  @media (min-width: 1200px) {
    ul {
      width: 100%;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      grid-template-rows: 1fr;
    }

    .toggle3 {
      display: block;
    }
  }

  .toggle-container {
    padding: 2rem;
    background-color: #97a5c0;
    width: 100%;
    height: 70%;
  }

  .basic-container {
    background-color: rgb(191 210 250);
    padding: 4rem 2rem;
  }

  .commingsoon-container {
    background-color: lightgrey;
    padding: 0;
    display: grid;
    align-items: center;
  }

  .toggle-info {
    display: grid;
    justify-items: flex-start;
    padding: 1rem;
  }
  .toggle-name {
    font-weight: 700;
    font-size: 1.25rem;
    line-height: 1.75rem;
  }

  .toggle-description {
    color: #6b7280;
    font-size: 0.875rem;
    line-height: 1.25rem;
    padding-top: 0.25rem;
    padding-bottom: 1.25rem;
  }

  .check-more {
    font-weight: 600;
    color: #4570e6;
  }
</style>
