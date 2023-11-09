<script>
  import anime from "animejs";

  const moonPath =
    "M100 50C100 77.6142 77.6142 100 50 100C22.3858 100 0 77.6142 0 50C0 22.3858 22.3858 0 50 0C46.0531 29.8513 67.0154 53.5842 100 50Z";

  const sunPath =
    "M100 50C100 77.6142 77.6142 100 50 100C22.3858 100 0 77.6142 0 50C0 22.3858 22.3858 0 50 0C77.6142 0 100 22.3858 100 50Z";

  let isCurrentThemeDark = false;

  function toggleSimple() {
    // Use anime.js
    const timeline = anime.timeline({
      duration: 650,
      easing: "easeOutExpo",
    });
    // Add animations to timeline
    timeline.add({
      targets: ".simple",
      d: [{ value: isCurrentThemeDark ? sunPath : moonPath }],
    });
    isCurrentThemeDark = !isCurrentThemeDark;
  }
</script>

<button on:click={toggleSimple}>
  <svg
    id="darkMode"
    width="100"
    height="100"
    viewBox="0 0 100 100"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
  >
    <path
      class="simple"
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M100 50C100 77.6142 77.6142 100 50 100C22.3858 100 0 77.6142 0 50C0 22.3858 22.3858 0 50 0C77.6142 0 100 22.3858 100 50Z"
      fill="#fff9d1"
    />
  </svg>
</button>

<style>
  svg {
    cursor: pointer;
    height: 10rem;
    width: 10rem;
    margin: 0;
  }
  button {
    background-color: transparent;
    border: none;
  }
</style>
