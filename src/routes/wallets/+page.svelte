<script lang = "ts">
    import { onMount } from "svelte";
    import Navbar from "../Navbar.svelte";

    let popularWallets;
    let pageLoaded = false;

    async function getPopularWallets() {
        // TODO: replace mocked data with API call
        return [
            "0x12345",
            "0x23456",
            "0x34567",
            "0x45678"
        ]
    }

    onMount(async() => {
        popularWallets = await getPopularWallets();
        pageLoaded = true;
    });
</script>

<Navbar />

<!-- placeholder -->
<div class = "main">
    <h2>Explore wallets!</h2>

    <p>Popular wallets:</p>

    {#if pageLoaded}
        <ul>
            {#each popularWallets as wallet}
                <li><a href = "/wallets/{wallet}">{wallet}</li>
            {/each}
        </ul>
    {/if}
</div>