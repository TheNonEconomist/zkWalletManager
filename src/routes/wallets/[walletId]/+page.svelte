<script lang="ts">
    import {page} from '$app/stores';
    import { onMount } from 'svelte';
    import WalletDisplay from "./WalletDisplay.svelte";

    let wallet: Record<string, string>

    $: walletId = $page.params.walletId;

    // TODO
    async function getWallet(id: string) {
        return {
            "id": id,
            "chains":[
                "bitcoin",
                "ethereum"
            ],
            "extlinks":[
                "twitter",
                "farcaster"
            ]
        }
    }

    onMount(async() => {
        wallet = await getWallet(walletId);
    })
</script>

<WalletDisplay wallet = {wallet}/>






