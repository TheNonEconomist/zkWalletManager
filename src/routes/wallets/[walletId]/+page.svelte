<script lang="ts">
    import {page} from '$app/stores';
    import { onMount } from 'svelte';
    import WalletDisplay from "./WalletDisplay.svelte";

    let wallet: Record<string, Record<string, string>>
    let pageLoaded: Boolean = false;

    $: walletId = $page.params.walletId;

    // TODO: replace with API call
    async function getWallet(id: string) {
        return {
            "id": id,
            "location": "123 ABCDEF, GHI, JKLM",
            "chains":{
                "bitcoin": "0x123",
                "ethereum": "0x456"
            },
            "extlinks":{
                "twitter": "lorem",
                "facebook": "ipsum"
            }
        }
    }

    onMount(async() => {
        wallet = await getWallet(walletId);
        pageLoaded = true;
    })
</script>

{#if pageLoaded == true}
    <WalletDisplay wallet = {wallet}/>
{/if}






