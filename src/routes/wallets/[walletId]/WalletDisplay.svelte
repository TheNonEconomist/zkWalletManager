<script>
    export let wallet;
    import locationpin from "../../../logos/location-pin.png";
    import LinkList from "./LinkList.svelte";
</script>

<!-- header-->
<h2>{wallet["id"]}</h2>

<p><img src = {locationpin} height = "32px"/> {wallet["location"]}</p>

<div class = "links">
    <!-- blockchain links-->
    <div class = "column">
        <h3>Wallets</h3>
        <LinkList linksToList = {wallet["chains"]} />
    </div>

    <!-- external links-->
    <div class = "column">
        <h3>External links</h3>
        <LinkList linksToList = {wallet["extlinks"]} />
    </div>
</div>