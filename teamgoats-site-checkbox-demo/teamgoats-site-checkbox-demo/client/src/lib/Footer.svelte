<script>
  import Github from "../assets/github-mark-white.svg";
</script>

<footer>
  <div>
    Svelte Toggle Switches, built by <a href="https://github.com/Team-GOATS"
      >Team GOATs</a
    >
  </div>
  <div>
    <a href="https://github.com/Team-GOATS">Team GOATS Logo</a>
    <a href="https://github.com/Team-GOATS" title="Out Github"
      ><img src={Github} alt="Github Logo" /></a
    >
  </div>
</footer>

<style>
  footer {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    border-top: #b6b6b6 1px solid;
    margin: 0 10rem;
    padding: 0;
  }
  footer div {
    margin: 1rem;
  }

  footer div img {
    width: 2rem;
  }
</style>
