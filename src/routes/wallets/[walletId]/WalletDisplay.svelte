<script>
    export let wallet;
</script>

<!-- header-->
<h2>{wallet["id"]}</h2>

<div class = "links">
    <!-- blockchain links-->
    <div class = "column">
        <h3>Wallets</h3>
        <ul>
            {#each Object.entries(wallet["chains"]) as [chain, username]}
                <li>{chain}: {username}</li>
            {/each}
        </ul>
    </div>

    <!-- external links-->
    <div class = "column">
        <h3>External links</h3>
        <ul>
            {#each Object.entries(wallet["extlinks"]) as [extsite, username]}
                <li>{extsite}: {username}</li>
            {/each}
        </ul>
    </div>

    <!-- sanity check-->
    <!-- <p>{JSON.stringify(wallet)}</p> -->
</div>