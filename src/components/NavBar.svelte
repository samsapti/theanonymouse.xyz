<script lang="ts">
  import ThemeSwitcher from "./ThemeSwitcher.svelte";
  import { Hamburger } from "svelte-hamburgers";
  import { onMount } from "svelte";

  // Props
  export let currentTab: string;
  export let isDark: boolean;
  export let name: string;
  export let tabs = [];

  let isMobile: boolean;
  let openMenu: boolean;

  // Set chosen or default tab
  function handleTab() {
    let hash = location.hash;
    openMenu = false;
    if (tabs.some((t) => t.href === hash)) currentTab = hash;
    else currentTab = location.hash = tabs[0].href;
  }

  // Code to run when navbar loads
  onMount(() => {
    // Responsive design
    const responsiveQuery = window.matchMedia("(min-width: 720px)");
    responsiveQuery.addEventListener("change", (e) => (isMobile = !e.matches));
    isMobile = !responsiveQuery.matches;

    // Set tab
    handleTab();
  });
</script>

<svelte:window on:hashchange={handleTab} />
<nav>
  {#if isMobile}
    <div id="hamburger">
      <Hamburger bind:open={openMenu} --color="white" />
    </div>
  {:else}
    <a id="name" href="/">{name}</a>
  {/if}
  {#if !isMobile || openMenu}
    <ul class:mobile={isMobile}>
      {#each tabs as { href, label }}
        <li>
          <a class="nav-item" class:here={currentTab === href} {href}>
            {label}
          </a>
        </li>
      {/each}
    </ul>
  {/if}
  <ThemeSwitcher bind:isDark />
</nav>

<style lang="scss">
  @import "../scss/colorscheme.scss";

  a {
    text-decoration: none;
    color: $white;
  }

  #name {
    color: $white;
    display: inline-block;
    font-size: 20px;
    padding: 0 24px;
    margin: auto 0;
  }

  #hamburger {
    cursor: pointer;
  }

  nav {
    background-color: $primary;
    display: flex;
    height: 58px;
  }

  .nav-item {
    padding: 24px;
    display: inline-flex;
  }

  .here,
  .nav-item:hover {
    background-color: $secondary;
    color: $black;
  }

  ul {
    margin: 0;
    padding: 0;
    list-style-type: none;
    display: flex;
    align-items: center;
    justify-content: flex-start;
  }

  ul.mobile {
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

  @media (min-width: 720px) {
    nav {
      height: auto;
    }
  }
</style>
