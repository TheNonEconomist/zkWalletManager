<script>
    export let wallet;
</script>

<!-- header-->
<h1>{wallet["id"]}</h1>

<!-- blockchain links-->
<h2>Other wallets</h2>
<ul>
    {#each wallet["chains"] as chain}
        <li>{chain}</li>
    {/each}
</ul>

<!-- external links-->
<h2>External links</h2>
<ul>
    {#each wallet["extlinks"] as extlink}
        <li>{extlink}</li>
    {/each}
</ul>

<!-- sanity check-->
<!-- <p>{JSON.stringify(wallet)}</p> -->