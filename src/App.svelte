<script lang="ts">
  import About from "./components/About.svelte";
  import InfoBar from "./components/InfoBar.svelte";
  import NavBar from "./components/NavBar.svelte";

  let currentTab: string;
  let tabs = [
    { label: "About", href: "#about" },
    { label: "Contact", href: "#contact" },
    { label: "Privacy Policy", href: "#privacy" },
    { label: "SearX", href: "https://searx.theanonymouse.xyz" },
  ];

  const name = "the_4n0nym0u53";
</script>

<div id="content">
  <header>
    <NavBar bind:currentTab {tabs} {name} />
  </header>

  <main>
    {#if currentTab === tabs[0].href}
      <About {name} />
    {/if}

    {#if currentTab === tabs[1].href}
      <h3>No content yet!</h3>
    {/if}

    {#if currentTab === tabs[2].href}
      <h3>No content yet!</h3>
    {/if}
  </main>

  <footer>
    <InfoBar />
  </footer>
</div>

<style lang="scss">
  @import "./scss/colorscheme.scss";

  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;

    background-color: var(--background);
    color: var(--text);
  }

  #content {
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    justify-content: space-between;
  }

  header, footer {
    width: 100%;
    margin: 0;
  }

  main {
    padding: 5em;
    display: flex;
    justify-content: center;
  }
</style>
