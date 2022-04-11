<script lang="ts">
  import { onMount } from "svelte";

  export let currentTab: string;
  export let tabs = [];
  export let name: string;

  // Reactively update URL hash
  $: window.location.hash = currentTab;

  // Tab handler function
  function handleTab() {
    let hash = window.location.hash;

    if (tabs.some((t) => t.href === hash)) currentTab = hash;
    else currentTab = tabs[0].href;
  }

  onMount(handleTab);
</script>

<svelte:window on:hashchange={handleTab} />
<nav>
  <a id="brand" href="/">{name}</a>
  <ul>
    {#each tabs as { href, label }}
      <li class:here={currentTab === href}>
        <a class="nav-item" {href} on:click={handleTab}>
          {label}
        </a>
      </li>
    {/each}
  </ul>
</nav>

<style lang="scss">
  @import "../scss/colorscheme.scss";

  a {
    text-decoration: none;
    color: $white;
  }

  #brand {
    color: $white;
    display: block;
    padding: 0 24px;
    font-size: 24px;
  }

  nav {
    background-color: $primary;
    display: flex;
    align-items: center;

    ul {
      margin: 0;
      padding: 0;
      list-style-type: none;
      display: flex;
      align-items: center;
      justify-content: flex-start;

      .nav-item {
        padding: 24px;
        display: block;
      }

      .here a,
      .nav-item:hover {
        background-color: $secondary;
        color: $black;
      }
    }
  }
</style>
