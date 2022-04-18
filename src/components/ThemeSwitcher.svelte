<script lang="ts">
  import SunIcon from "@inqling/svelte-icons/solid/sun.svelte";
  import MoonIcon from "@inqling/svelte-icons/solid/moon.svelte";
  import { onMount } from "svelte";

  // Prop
  export let isDark: boolean;

  // Get dark theme
  function getDark() {
    let dark = localStorage.getItem("dark");
    if (dark != null) return dark == "true";
    return window.matchMedia("(prefers-color-scheme: dark)").matches;
  }

  // Toggle theme
  function toggleTheme() {
    isDark = !isDark;
    localStorage.setItem("dark", `${isDark}`);
  }

  onMount(() => {
    const themeQuery = window.matchMedia("(prefers-color-scheme: dark)");
    themeQuery.addEventListener("change", () => (isDark = getDark()));
    isDark = getDark();
  });
</script>

<button
  title="Switch to {isDark ? 'light' : 'dark'} theme"
  on:click={toggleTheme}
>
  {#if isDark}
    <SunIcon id="icon" />
  {:else}
    <MoonIcon id="icon" />
  {/if}
</button>

<style lang="scss">
  @import "../scss/colorscheme.scss";

  button {
    background-color: $black;
    color: $accent2;
    border: 3px solid $accent1;
    border-radius: 50%;
    height: 32px;
    width: 32px;
    margin: auto;
    margin-right: 2vh;
    padding: 3px;
    cursor: pointer;
  }

  @media (min-width: 720px) {
    button {
      height: 38px;
      width: 38px;
    }
  }
</style>
