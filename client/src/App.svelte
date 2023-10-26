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
  main {
    color: #f5f5f5;
    text-align: center;
    display: flex;
    flex-direction: column;
    gap: 30px;
  }

  .contentBox {
    display: flex;
    flex-direction: column;
    gap: 30px;
  }
  p {
    margin: 4rem auto;
  }

  .titleSection {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 10px;
  }

  .titleSection h1 {
    background: linear-gradient(to right, #2563eb, #3eadcf);
    -webkit-background-clip: text; /* For compatibility with some web browsers */
    background-clip: text;
    color: transparent;
    margin-top: 25px;
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
    transition: all 0.4s ease-in-out;
  }

  .titleSection a:hover {
    color: #4570e6;
    font-size: 32px;
    text-decoration: underline;
  }
</style>
