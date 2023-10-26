<script>
  import Header from "./lib/Header.svelte";
  import Footer from "./lib/Footer.svelte";
  import ToggleLists from "./lib/ToggleLists.svelte";
</script>

<main class="container">
  <Header />
  <div class="contentBox">
    <section class="titleSection">
      <h1>Svelte Toggle Switches</h1>
      <p>
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Incidunt, modi
        tempore temporibus sint quis quaerat fugiat necessitatibus, consequatur
        eum architecto corporis, accusamus quos sapiente qui? Odio at odit
        reiciendis dolorum!
      </p>
      <a href="https://github.com/Team-GOATS/svelte-toggles-npm-package"
        >GET STARTED</a
      >
    </section>

    <section>
      <ToggleLists />
    </section>
  </div>

  <Footer />
</main>

<style>
  .container {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 100%;
    min-height: 100vh;
    margin: 0 auto;
    color: #f5f5f5;
    text-align: center;
    position: relative;
  }

  .contentBox {
    max-width: 1300px;
    align-self: center;
    justify-self: start;
  }

  a {
    color: #f5f5f5;
    text-decoration: none;
    transition: all 0.5s ease-in-out;
=======
</script>

<main>
  <h1>Svelte Toggle Switches</h1>
  <h2>Coming Soon</h2>
  <p>
    To keep updated on latest developments, check out our <a
      href="https://github.com/Team-GOATS"
      target="_blank"
      rel="noreferrer">GitHub</a
    >
  </p>
</main>

<style>
  main {
    color: #f5f5f5;
    text-align: center;
    margin: 10rem auto;
  }
  h2 {
    color: #0284c7;
  }
  p {
    margin: 4rem auto;
  }
  a {
    color: #f5f5f5;
    text-decoration: none;
    transition: all 0.6s ease-in-out;
>>>>>>> b6a0b2bff739c6e89a34574b7604d8f7968fb118
  }
  a:hover {
    color: #0284c7;
  }
<<<<<<< HEAD

  .titleSection {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .titleSection h1 {
    background: linear-gradient(to right, #2563eb, #3eadcf);
    -webkit-background-clip: text; /* For compatibility with some web browsers */
    background-clip: text;
    color: transparent;
    margin-top: 20px;
  }

  .titleSection p {
    margin: 20px;
    width: 80%;
  }
  .titleSection a {
    color: #4a90e2;
    font-size: 30px;
    font-weight: bold;
    margin-top: 20px;
    margin-bottom: 40px;
  }

  .titleSection a:hover {
    color: #235dab;
    font-size: 30px;
    text-decoration: underline;
  }
=======
>>>>>>> b6a0b2bff739c6e89a34574b7604d8f7968fb118
</style>
