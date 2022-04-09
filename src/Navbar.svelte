<script lang="ts">
    import { onMount } from "svelte";

    export let currentTab: number;
    export let name: string;
    export let tabs = [];

    // Set default tab to About page
    onMount(() => {
        if (Array.isArray(tabs) && tabs.length && tabs[0].value) {
            currentTab = tabs[0].value;
        }
    });
</script>

<nav>
    <a id="brand" href="/">{name}</a>
    <ul>
        {#if Array.isArray(tabs)}
            {#each tabs as tab}
                <li class:here={currentTab === tab.value}>
                    <span
                        class="nav-item"
                        on:click={() => (currentTab = tab.value)}
                    >
                        {tab.label}
                    </span>
                </li>
            {/each}
        {/if}
        <li>
            <a class="nav-item" href="https://searx.theanonymouse.xyz">
                SearX
            </a>
        </li>
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

    #brand {
        display: block;
        padding: 0 24px;
        font-size: 24px;
    }

    nav {
        background-color: #333333;
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
                color: #e7e7e7;
                padding: 24px;
                display: block;
            }

            .here,
            .nav-item:hover,
            .nav-item:focus {
                background-color: #272727;
            }
        }
    }
</style>
