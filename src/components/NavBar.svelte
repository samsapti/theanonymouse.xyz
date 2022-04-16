<script lang="ts">
  import { Hamburger } from "svelte-hamburgers";
  import { onMount } from "svelte";
  import SunIcon from "@inqling/svelte-icons/solid/sun.svelte";
  import MoonIcon from "@inqling/svelte-icons/solid/moon.svelte";

  export let currentTab: string;
  export let isDark: boolean;
  export let tabs = [];

  let isMobile: boolean;
  let openMenu: boolean;

  // Set chosen or default tab
  function handleTab() {
    let hash = location.hash;
    if (openMenu) openMenu = false;

    if (tabs.some((t) => t.href === hash)) currentTab = hash;
    else currentTab = location.hash = tabs[0].href;
  }

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

  // Code to run when navbar loads
  onMount(() => {
    // Responsive design
    const responsiveQuery = window.matchMedia("(min-width: 720px)");
    responsiveQuery.addEventListener("change", (e) => (isMobile = !e.matches));
    isMobile = !responsiveQuery.matches;

    // Set theme
    const themeQuery = window.matchMedia("(prefers-color-scheme: dark)");
    themeQuery.addEventListener("change", () => (isDark = getDark()));
    isDark = getDark();

    // Set tab
    handleTab();
  });
</script>

<svelte:window on:hashchange={handleTab} />
<div id="content">
  <nav>
    {#if isMobile}
      <div id="mobile-icon">
        <Hamburger bind:open={openMenu} --color="white" />
      </div>
    {:else}
      <a id="name" href="/">the_4n0nym0u53</a>
    {/if}
    {#if !isMobile || openMenu}
      <ul id="nav-list" class:mobile={isMobile}>
        {#each tabs as { href, label }}
          <li class:here={currentTab === href}>
            <a class="nav-item" {href} on:click={handleTab}>
              {label}
            </a>
          </li>
        {/each}
      </ul>
    {/if}
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
  </nav>
</div>

<style lang="scss">
  @import "../scss/colorscheme.scss";

  a {
    text-decoration: none;
    color: $white;
  }

  #content {
    width: 100%;
    padding: 0;
    margin: 0;
  }

  #name {
    color: $white;
    display: inline-block;
    font-size: 20px;
    padding: 0 24px;
    margin: auto 0;
  }

  nav {
    background-color: $primary;
    display: flex;
    height: 58px;

    #mobile-icon {
      cursor: pointer;
    }

    #nav-list {
      margin: 0;
      padding: 0;
      list-style-type: none;
      display: flex;
      align-items: center;
      justify-content: flex-start;
    }

    #nav-list.mobile {
      position: absolute;
      top: 58px;
      width: 100%;
      flex-direction: column;
      align-items: flex-start;
      justify-content: space-between;
      background-color: $primary;

      .nav-item {
        width: calc(100vw - 48px);
      }
    }

    .nav-item {
      padding: 24px;
      display: inline-flex;
    }

    .here a,
    .nav-item:hover {
      background-color: $secondary;
      color: $black;
    }

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
  }

  @media (min-width: 720px) {
    nav {
      height: auto;

      button {
        height: 38px;
        width: 38px;
      }
    }
  }
</style>
