<script>
  import logo from "../assets/team goats logo.png";

  let currentYear = new Date().getFullYear();

  function updateYear() {
    currentYear = new Date().getFullYear();
  }
</script>

<footer class="footer">
  <h3>TEAM GOATS</h3>
  <a href="https://github.com/Team-GOATS/svelte-toggles-npm-package">
    <img src={logo} alt="github logo" />
  </a>

  <span>&copy;{currentYear} Team Goats - Holmseglen</span>
</footer>

<style>
  .footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-self: center;
    margin: 1rem;
  }

  .footer img {
    width: 3.5rem;
    margin: 0.5rem;
  }
</style>
