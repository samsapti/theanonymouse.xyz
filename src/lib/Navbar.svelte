<script lang="ts">
  import { onMount } from "svelte";

  export let currentTab: number;
  export let siteName: string;
  export let tabs = [];

  onMount(() => {
    // Set default tab value
    if (Array.isArray(tabs) && tabs.length && tabs[0].value) {
      currentTab = tabs[0].value;
    }
  });
</script>

<nav>
  <a class="brand" href="/">{siteName}</a>
  <ul>
    {#if Array.isArray(tabs)}
      {#each tabs as tab}
        <li class:here={currentTab === tab.value}>
          <span on:click={() => (currentTab = tab.value)}> {tab.label} </span>
        </li>
      {/each}
    {/if}
  </ul>
</nav>

<style lang="scss">
  a {
    text-decoration: none;
  }

  a,
  span {
    color: #e7e7e7;
  }

  .brand {
    display: block;
    padding: 0 24px;
    font-size: 24px;
  }

  nav {
    background-color: #555555;
    display: flex;
    align-items: center;

    ul {
      margin: 0;
      padding: 0;
      list-style-type: none;
      display: flex;
      align-items: center;
      justify-content: flex-start;

      li span {
        color: #e7e7e7;
        padding: 24px;
        display: block;
      }

      span:hover,
      span:focus,
      .here {
        background-color: #272727;
      }
    }
  }
</style>
