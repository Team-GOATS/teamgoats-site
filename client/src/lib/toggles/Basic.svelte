<script>
    import anime from "animejs";
  
    const moonPath =
      "M21.5 50C21.5 77.6142 50 100 50 100C22.3858 100 0 77.6142 0 50C0 22.3858 22.3858 0 50 0C50 0 21.5 22.3858 21.5 50Z";
  
    const sunPath =
      "M100 50C100 77.6142 77.6142 100 50 100C22.3858 100 0 77.6142 0 50C0 22.3858 22.3858 0 50 0C77.6142 0 100 22.3858 100 50Z";
  
    let isCurrentThemeDark = false;
  
    function toggleBasic() {
      // Use anime.js
      const timeline = anime.timeline({
        duration: 750,
        easing: "easeOutExpo",
      });
      // Add animations to timeline
      timeline.add({
        targets: ".basic",
        d: [{ value: isCurrentThemeDark ? sunPath : moonPath }],
      });
      isCurrentThemeDark = !isCurrentThemeDark;
    }
  </script>
  
  <button on:click={toggleBasic} class="basic-btn">
    <svg
      id="darkMode"
      width="100"
      height="100"
      viewBox="0 0 100 100"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        class="basic"
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
  