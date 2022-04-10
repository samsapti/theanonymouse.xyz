<script lang="ts">
    import svelte from "./assets/svelte.png";
    import Navbar from "./Navbar.svelte";
    import About from "./About.svelte";

    const name = "the_4n0nym0u53";

    let currentTab: string;
    let tabs = [
        { label: "About", href: "#about" },
        { label: "Contact", href: "#contact" },
        { label: "Privacy Policy", href: "#privacy" },
    ];
</script>

<header>
    <Navbar bind:currentTab {name} {tabs} />
</header>

<main>
    {#if currentTab === tabs[0].href}
        <About {name} />
    {/if}

    {#if currentTab === tabs[1].href}
        <h3>Tab 2 content</h3>
    {/if}

    {#if currentTab === tabs[2].href}
        <h3>Tab 3 content</h3>
    {/if}
</main>

<footer>
    <span>
        This site is built with <a href="https://svelte.dev">Svelte.js</a>
        <img src={svelte} alt="Svelte.js logo" />
    </span>
</footer>

<style lang="scss">
    :root {
        font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
            Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
    }

    header,
    main,
    footer {
        text-align: center;
    }

    header {
        margin: 0;
        padding: 0;
    }

    main {
        padding: 10em;
        margin: 0 auto;
    }

    footer {
        margin: 0;
        padding: 0;

        span {
            font-size: small;

            img {
                height: 1em;
                width: 1em;
            }
        }
    }
</style>
