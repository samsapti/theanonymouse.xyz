<script lang="ts">
  import { onMount } from "svelte";
  import { Hamburger } from "svelte-hamburgers";

  export let currentTab: string;
  export let tabs = [];

  let isMobile: boolean;
  let openMenu: boolean;

  const mediaQueryHandler = (e: MediaQueryListEvent) => (isMobile = e.matches);
  const handleTab = () => {
    let hash = window.location.hash;
    if (openMenu) openMenu = false;

    if (tabs.some((t) => t.href === hash)) currentTab = hash;
    else currentTab = window.location.hash = tabs[0].href;
  };

  onMount(() => {
    const mediaQuery = window.matchMedia("(max-width: 680px)");
    mediaQuery.addEventListener("change", mediaQueryHandler, true);
    isMobile = mediaQuery.matches;
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
    {/if}
    <a id="name" href="/">the_4n0nym0u53</a>
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
    font-size: 24px;
    padding: 0 24px;
    margin: auto 0;
  }

  nav {
    background-color: $primary;
    display: flex;
    align-items: center;

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

    .nav-item {
      padding: 24px;
      display: inline-flex;
    }

    .here a,
    .nav-item:hover {
      background-color: $secondary;
      color: $black;
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
  }

  @media (max-width: 680px) {
    #content {
      align-items: flex-end;
    }

    nav {
      align-items: flex-start;
      justify-content: space-between;
    }
  }
</style>
