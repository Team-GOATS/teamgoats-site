<script>
  import anime from "animejs";

  const moonPath =
    "M90 40C90 40 72.0914 40 50 40C27.9086 40 10 40 10 40C10 17.9086 27.9086 0 50 0C72.0914 0 90 17.9086 90 40Z";

  const sunPath =
    "M90 40C90 62.0914 72.0914 80 50 80C27.9086 80 10 62.0914 10 40C10 17.9086 27.9086 0 50 0C72.0914 0 90 17.9086 90 40Z";

  let isCurrentThemeDark = false;

  function toggleHorizon() {
    // Use anime.js
    const timeline = anime.timeline({
      duration: 450,
      easing: "linear",
    });
    // Add animations to timeline
    timeline.add({
      targets: ".horizon",
      translateY: isCurrentThemeDark ? 0 : 40,
      d: [{ value: isCurrentThemeDark ? sunPath : moonPath }],
    });
    isCurrentThemeDark = !isCurrentThemeDark;
  }
</script>

<button on:click={toggleHorizon}>
  <svg
    id="darkMode"
    width="100"
    height="100"
    viewBox="0 0 100 100"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
  >
    <path
      d="M0 90C0 88.3431 1.34315 87 3 87H97C98.6569 87 100 88.3431 100 90C100 91.6569 98.6569 93 97 93H3C1.34314 93 0 91.6569 0 90Z"
      fill="#fff9d1"
    />

    <path
      class="horizon"
      d="M90 40C90 62.0914 72.0914 80 50 80C27.9086 80 10 62.0914 10 40C10 17.9086 27.9086 0 50 0C72.0914 0 90 17.9086 90 40Z"
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
