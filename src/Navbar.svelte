<script lang="ts">
    import { onMount } from "svelte";

    export let currentTab: string;
    export let name: string;
    export let tabs = [];

    // Tab switch handler function
    function handleTabSwitch() {
        let hash = window.location.hash;
        currentTab = (hash.length === 0 ? tabs[0].href : hash)
    }

    // Set default tab to About page
    onMount(handleTabSwitch);
</script>

<svelte:window on:hashchange={handleTabSwitch} />

<nav>
    <a id="brand" href="/">{name}</a>
    <ul>
        {#if Array.isArray(tabs)}
            {#each tabs as { href, label }}
                <li class:here={currentTab === href}>
                    <a class="nav-item" {href} on:click={handleTabSwitch}>
                        {label}
                    </a>
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

    a {
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
