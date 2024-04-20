<script lang = "ts">
    export let wallet;
</script>

<!-- header-->
<h1>{wallet["id"]}</h1>

<div class = "links">
    <!-- blockchain links-->
    <div class = "column">
        <h2>Wallets</h2>
        <ul>
            {#each Object.entries(wallet["chains"]) as [chain, username]}
                <li>{chain}: {username}</li>
            {/each}
        </ul>
    </div>

    <!-- external links-->
    <div class = "column">
        <h2>External links</h2>
        <ul>
            {#each Object.entries(wallet["extlinks"]) as [extsite, username]}
                <li>{extsite}: {username}</li>
            {/each}
        </ul>
    </div>

    <!-- sanity check-->
    <!-- <p>{JSON.stringify(wallet)}</p> -->
</div>