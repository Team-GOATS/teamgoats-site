<script>
  import Basic from "svelte-toggles/src/Basic";
  import Github from "../assets/github-mark-white.svg";
</script>

<header>
  <Basic size="small"/>
  <nav>
    <a href="https://github.com/Team-GOATS/svelte-toggles-npm-package"
      >Toggles</a
    >
    <a href="https://github.com/Team-GOATS/svelte-toggles-npm-package">About</a>
    <a href="https://github.com/Team-GOATS/svelte-toggles-npm-package"
      >Documentation</a
    >
  </nav>
  <div>
    <a href="https://github.com/Team-GOATS" title="Our Github"
      ><img src={Github} alt="Github Logo" /></a
    >
  </div>
</header>

<style>
  header {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    padding: 2rem;
  }
  header nav a {
    margin: 0 1.5rem;
    text-decoration: none;
    color: #b6b6b6;
    font-weight: bold;
    transition: all 0.5s ease-in-out;
  }
  header nav a:hover,
  header nav a:target {
    color: #f5f5f5;
  }
  header img {
    width: 2rem;
  }
</style>
