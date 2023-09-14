<script>
  import { onMount } from "svelte";
  const STORAGE_KEY = "theme";
  const DARK_PREFERENCE = "(prefers-color-scheme: dark)";

 

  const THEMES = {
    DARK: "dark",
    LIGHT: "light",
  };

  const prefersDarkThemes = () => window.matchMedia(DARK_PREFERENCE).matches;

  let currentTheme;
  const applyTheme = () => {
    const preferredTheme = prefersDarkThemes() ? THEMES.DARK : THEMES.LIGHT;
    currentTheme = localStorage.getItem(STORAGE_KEY) ?? preferredTheme;

    currentTheme = localStorage.getItem(STORAGE_KEY) ?? preferredTheme;

    if (currentTheme === THEMES.DARK) {
      document.body.classList.remove(THEMES.LIGHT);
      document.body.classList.add(THEMES.DARK);
    } else {
      document.body.classList.remove(THEMES.DARK);
      document.body.classList.add(THEMES.LIGHT);
    }
  };

  const toggleTheme = () => {
    const stored = localStorage.getItem(STORAGE_KEY);

    if (stored) {
      localStorage.removeItem(STORAGE_KEY);
    } else {
      localStorage.setItem(
        STORAGE_KEY,
        prefersDarkThemes() ? THEMES.LIGHT : THEMES.DARK
      );
    }
    var animation_ease = Linear.easeNone;
  var animation_water = new TimelineMax({
  repeat: -1, 
  yoyo: true
});
animation_water
  .to("#dash", 2, {y: 12, morphSVG:"#water-2", ease: animation_ease}, 0 , 0)
;
    applyTheme();
  };

  onMount(() => {
    applyTheme();
    window.matchMedia(DARK_PREFERENCE).addEventListener("change", applyTheme);
  });
</script>

<label class="themeToggle" title="Toggle Theme">
  <input
    type="checkbox"
    checked={currentTheme !== THEMES.LIGHT}
    on:click={toggleTheme}
  />
  <span class="theme-toggle-sr">Toggle theme</span>
</label>

<style>
 
  span {
    display: none;
  }
</style>
