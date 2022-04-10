<script lang="ts">
  import Navbar from "./Navbar.svelte";
  import About from "./About.svelte";

  import github from "./assets/github-logo.svg";
  import license from "./assets/cc-logo.svg";

  let currentTab: string;
  let tabs = [
    { label: "About", href: "#about" },
    { label: "Contact", href: "#contact" },
    { label: "Privacy Policy", href: "#privacy" },
    { label: "SearX", href: "https://searx.theanonymouse.xyz" },
  ];

  const name = "the_4n0nym0u53";
</script>

<header>
  <Navbar bind:currentTab {tabs} {name} />
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
  <span>
    Source code can be found on
    <a
      target="_blank"
      href="https://github.com/theanonymousexyz/theanonymouse.xyz"
    >
      GitHub
      <img src={github} alt="GitHub logo" />
    </a>
  </span>
  <span>
    Licensed under
    <a target="_blank" href="https://creativecommons.org/licenses/by-nc-sa/4.0">
      CC BY-NC-SA 4.0
      <img
        src={license}
        alt="Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International"
      />
    </a>
  </span>
</footer>

<style lang="scss">
  @import "./colors.scss";

  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;

    background-color: $lightgray;
  }

  main {
    padding: 5em;
    padding-bottom: 3rem;
    display: flex;
    justify-content: center;
  }

  footer {
    position: fixed;
    bottom: 0;
    display: flex;
    justify-content: center;
    width: 100%;

    span {
      font-size: 1rem;
      margin: 1em;

      a {
        text-decoration: none;
      }

      img {
        height: 1em;
      }
    }
  }
</style>
