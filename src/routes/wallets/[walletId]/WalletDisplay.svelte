<script>
    export let wallet;
</script>

<!-- header-->
<h1>{wallet["id"]}</h1>

<!-- blockchain links-->
<h2>Other wallets</h2>
<ul>
    <li>{JSON.stringify(wallet["chains"])}</li>
</ul>

<!-- external links-->
<h2>External links</h2>
<ul>
    <li>{JSON.stringify(wallet["extlinks"])}</li>
</ul>

<!-- sanity check-->
<p>{JSON.stringify(wallet)}</p>