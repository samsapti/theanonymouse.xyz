<script lang="ts">
  import About from "./pages/About.svelte";
  import Contact from "./pages/Contact.svelte";
  import PrivacyPolicy from "./pages/PrivacyPolicy.svelte";
  import Donate from "./pages/Donate.svelte";
  import Footer from "./components/Footer.svelte";
  import NavBar from "./components/NavBar.svelte";

  let currentTab: string;
  let isDark: boolean;
  let name = "the_4n0nym0u53";
  let tabs = [
    { href: "#about", label: "About" },
    { href: "#contact", label: "Contact" },
    { href: "#donate", label: "Donate" },
    { href: "#privacy", label: "Privacy Policy" },
  ];
</script>

<div id="content" class:dark={isDark}>
  <header>
    <NavBar bind:currentTab bind:isDark {name} {tabs} />
  </header>
  <main>
    {#if currentTab === tabs[0].href}
      <About />
    {:else if currentTab === tabs[1].href}
      <Contact />
    {:else if currentTab === tabs[2].href}
      <Donate />
    {:else if currentTab === tabs[3].href}
      <PrivacyPolicy />
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
  }

  :global(html),
  :global(body) {
    margin: 0;
    padding: 0;
  }

  #content {
    background-color: $bg-light;
    color: $black;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    justify-content: space-between;
  }

  #content.dark {
    background-color: $bg-dark;
    color: $white;
  }

  header,
  footer {
    width: 100%;
    margin: 0;
    padding: 0;
  }

  main {
    padding: 6em;
    margin: 0;
    display: flex;
    justify-content: center;
  }
</style>
