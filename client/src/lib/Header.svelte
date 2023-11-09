<script>
  import Basic from "svelte-toggles/src/Basic";
  import Github from "../assets/githubIcon.svg";

  let isClassAdded = false;
  function toggleClass() {
    isClassAdded = !isClassAdded;
  }
</script>

<header class="headerContainer">
  <Basic fill="rgb(168, 168, 168)" />
  <nav class="nav" class:show={isClassAdded}>
    <a
      class="headerLink navLink"
      href="https://github.com/Team-GOATS/svelte-toggles-npm-package#user-content-toggles"
      >Toggles</a
    >

    <a
      class="headerLink navLink"
      href="https://github.com/Team-GOATS/svelte-toggles-npm-package#readme"
      >Documentation</a
    >

    <a class="headerLink navLink" href="https://github.com/Team-GOATS"
      >About Us</a
    >
  </nav>

  <a
    class="github headerLink"
    class:show={isClassAdded}
    href="https://github.com/Team-GOATS/svelte-toggles-npm-package"
  >
    <img class="headerImg" src={Github} alt="github icon" />
  </a>

  <button class="menuBtn" on:click={toggleClass}>
    <svg
      xmlns="http://www.w3.org/2000/svg"
      width="24"
      height="17"
      viewBox="0 0 24 17"
      aria-label=""
      class="svg-replaced"
      shape-rendering="geometricPrecision"
    >
      <path d="M0 0h24v3H0zm0 7h24v3H0zm0 7h24v3H0z" fill-rule="evenodd" />
    </svg>
  </button>
</header>

<style>
  .headerContainer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 4.5rem;
    position: relative;
    font-size: 1.4rem;
    padding-left: 10%;
    padding-right: 10%;
    margin-top: 1rem;
    width: 100%;
    max-width: 1400px;
  }

  .headerLink {
    padding: 10px;
    display: block;
  }

  .nav {
    display: flex;
    align-items: center;
    flex-direction: row;
    gap: 10px;
    display: none;
  }

  .navLink {
    transition: all 0.4s ease-in-out;
  }
  .navLink:hover {
    color: #4570e6;
  }

  .github {
    display: none;
    height: 3.5rem;
  }
  .nav.show {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 0;
    position: absolute;
    top: 60px;
    left: 0;
    width: 100vw;
    padding: 60px 0 15px 0;
    background-color: lightgray;
  }

  .github.show {
    display: flex;
    position: absolute;
    left: 0;
    top: 60px;
    width: 100vw;
    padding-left: 2.1rem;
    background-color: lightgray;
  }

  .github.show img {
    background-color: lightgray;
  }

  .menuBtn {
    background: none;
    border: 1px solid #cfd7de;
    border-radius: 4px;
    display: flex;
    margin: 15px;
    padding: 10px;
  }

  .menuBtn:hover {
    cursor: pointer;
  }

  @media (min-width: 780px) {
    .headerContainer {
      padding: 0;
      width: 80%;
      max-width: 1400px;
    }

    .nav {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
    }

    .github {
      display: flex;
    }

    .menuBtn {
      display: none;
    }
  }
</style>
