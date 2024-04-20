<script lang = "ts">
    export let wallet;
</script>

<!-- header-->
<h1>{wallet["id"]}</h1>

<!-- blockchain links-->
<h2>Other wallets</h2>
<ul>
    {#each Object.entries(wallet["chains"]) as [chain, username]}
        <li>{chain}: {username}</li>
    {/each}
</ul>

<!-- external links-->
<h2>External links</h2>
<ul>
    {#each Object.entries(wallet["extlinks"]) as [extsite, username]}
        <li>{extsite}: {username}</li>
    {/each}
</ul>

<!-- sanity check-->
<!-- <p>{JSON.stringify(wallet)}</p> -->