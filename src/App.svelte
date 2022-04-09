<script lang="ts">
  import src from "./assets/theanonymouse.png";
  import Navbar from "./lib/Navbar.svelte";

  const siteName = "the_4n0nym0u53";
  let currentTab: number;

  let tabs = [
    { label: "About", value: 1 },
    { label: "Blog", value: 2 },
    { label: "Contact", value: 3 },
    { label: "Privacy Policy", value: 4 },
  ];
</script>

<header>
  <Navbar bind:currentTab {siteName} {tabs} />
</header>

<main>
  <img {src} alt="the_4n0nym0u53 profile" />
  <h1>Hello from {siteName}!</h1>
  <p>Welcome to my website!</p>

  {#if currentTab === 1}
    <h3>Tab 1 content</h3>
  {/if}

  {#if currentTab === 2}
    <h3>Tab 2 content</h3>
  {/if}

  {#if currentTab === 3}
    <h3>Tab 3 content</h3>
  {/if}
</main>

<style lang="scss">
  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  }

  header {
    margin: 0;
    padding: 0;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }

  img {
    height: 16rem;
    width: 16rem;
  }

  h1 {
    color: #ff3e00;
    font-size: 4rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 14rem;
  }

  p {
    max-width: 14rem;
    margin: 1rem auto;
    line-height: 1.35;
  }

  @media (min-width: 480px) {
    h1 {
      max-width: none;
    }

    p {
      max-width: none;
    }
  }
</style>
