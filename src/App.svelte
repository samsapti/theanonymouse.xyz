<script lang="ts">
  import About from "./components/About.svelte";
  import Footer from "./components/Footer.svelte";
  import NavBar from "./components/NavBar.svelte";

  let currentTab: string;
  let tabs = [
    { label: "About", href: "#about" },
    { label: "Contact", href: "#contact" },
    { label: "Privacy Policy", href: "#privacy" },
    { label: "SearX", href: "https://searx.theanonymouse.xyz" },
  ];
</script>

<div id="content">
  <header>
    <NavBar bind:currentTab {tabs} />
  </header>
  <main>
    {#if currentTab === tabs[0].href}
      <About />
    {:else if currentTab === tabs[1].href}
      <h3>No content yet!</h3>
    {:else if currentTab === tabs[2].href}
      <h3>No content yet!</h3>
    {/if}
  </main>
  <footer>
    <Footer />
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

  header,
  footer {
    width: 100%;
    margin: 0;
  }

  main {
    padding: 5em;
    display: flex;
    justify-content: center;
  }
</style>
