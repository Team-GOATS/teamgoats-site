<script>
  let isClassAdded = false;
  function toggleClass() {
    isClassAdded = !isClassAdded;
  }

  // <button on:click={toggleClass}>Toggle Class</button>

  // <div class:classname={isClassAdded ? 'added-class' : ''}>
  //   This div can have a class added or removed.
  // </div>
</script>

<header class="headerContainer">
  <a class="headerLink logo" href="/">
    <img class="headerImg" src="../src/img/logo.png" alt="logo" />
    <span class="logoName">THE GOATS</span>
    <img
      class="headerImg modeSwitch"
      src="../src/img/moon.svg"
      alt="dark light mode"
    />
  </a>

  <nav class="nav" class:show={isClassAdded}>
    <a
      class="headerLink"
      href="https://github.com/Team-GOATS/svelte-toggles-npm-package">Toggles</a
    >
    <a
      class="headerLink"
      href="https://github.com/Team-GOATS/svelte-toggles-npm-package">About</a
    >
    <a
      class="headerLink"
      href="https://github.com/Team-GOATS/svelte-toggles-npm-package"
      >Documentation</a
    >
  </nav>

  <a
    class="github headerLink"
    class:show={isClassAdded}
    href="https://github.com/Team-GOATS/svelte-toggles-npm-package"
  >
    <img class="headerImg" src="../src/img/githubIcon.svg" alt="github icon" />
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
    height: 60px;
    position: relative;
    font-size: 20px;
  }

  .headerImg {
    /* display: block; */
    height: 35px;
  }

  .headerLink {
    padding: 10px;
    display: block;
    color: #f5f5f5;
  }

  .logo {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 5px;
  }

  .modeSwitch {
    margin-left: 30px;
  }

  .nav {
    display: flex;
    align-items: center;
    flex-direction: row;
    gap: 10px;
    display: none;
  }

  .github {
    display: none;
  }
  .nav.show {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 0;
    position: absolute;
    top: 60px;
    width: 100vw;
    padding: 20px;
    padding-top: 60px;
    background-color: lightgray;
  }

  .github.show {
    display: flex;
    position: absolute;
    left: 0;
    top: 60px;
    width: 100vw;
    padding-left: 20px;
    background-color: lightgray;
  }

  .nav a {
    color: #f5f5f5;
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

  .menuBtn::active .nav {
    display: block;
    margin: 10px 20px;
    fill: #14a96d;
  }

  @media (min-width: 780px) {
    .nav {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
    }

    .github {
      display: flex;
    }
    /* .nav.show {
      position: relative;
      display: flex;
      flex-direction: row;
      top: 0;
      background-color: white;
      padding: 0, 20px;
      width: 80%;
    } */

    .menuBtn {
      display: none;
    }
  }
</style>
