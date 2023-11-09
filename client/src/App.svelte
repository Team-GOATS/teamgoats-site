<script>
  import Header from "./lib/Header.svelte";
  import Footer from "./lib/Footer.svelte";
  import Basic from "./lib/toggles/Basic.svelte";
  import Simple from "./lib/toggles/Simple.svelte";
  import Horizon from "./lib/toggles/Horizon.svelte";
</script>

<main>
  <Header />

  <section class="intro-section">
    <h1>Svelte Toggle Switches</h1>

    <p>
      Svelte Toggles Switches - your one-stop shop for Light & Dark mode
      solution! We've got all the Local Storage mumbo-jumbo covered; all you
      need is your creative touch to switch themes. <br /><br /> Svelte Toggles will
      continue to be maintained, ensuring you have reliable support in the long run.
      So why break a sweat when you can switch with a smile? Join the Svelte Toggles
      revolution today!
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

      <li>
        <div class="toggle-container simple-container">
          <Simple />
        </div>
        <a href="https://github.com/Team-GOATS/svelte-toggles-npm-package">
          <div class="toggle-info">
            <h3 class="toggle-name">Simple</h3>
            <p class="toggle-description">Sun Morphs into Moon</p>
            <p class="check-more">Check More</p>
          </div>
        </a>
      </li>

      <li>
        <div class="toggle-container horizon-container">
          <Horizon />
        </div>
        <a href="https://github.com/Team-GOATS/svelte-toggles-npm-package">
          <div class="toggle-info">
            <h3 class="toggle-name">Horizon</h3>
            <p class="toggle-description">Sun falls behind Horizon</p>
            <p class="check-more">Check More</p>
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
    width: 100%;
  }

  ul {
    width: 100%;
    display: grid;
    grid-template-columns: repeat(1, minmax(10rem, 20rem));
    row-gap: 3rem;
    /* column-gap: 2rem; */
  }

  li {
    list-style: none;
    border-radius: 0.375rem;
    overflow: hidden;
    transition-property: all;
    transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
    transition-duration: 0.15s;
    /* width: 100%; */
  }

  li:hover {
    transform: scale(1.05);
  }

  .toggle-container {
    padding: 4rem;
  }

  .basic-container {
    background-color: rgb(191 210 250);
  }

  .simple-container {
    background-color: #bcdb9c;
  }

  .horizon-container {
    background-color: #cfbaff;
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

  @media (min-width: 768px) {
    ul {
      grid-template-columns: 1fr 1fr;
      grid-template-rows: 1fr 1fr;
      gap: 3rem;
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
  }
</style>
