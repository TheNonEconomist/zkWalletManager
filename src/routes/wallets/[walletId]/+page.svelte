<script lang="ts">
    import {page} from '$app/stores';
    import { onMount } from 'svelte';

    let wallet: Record<string, string>

    $: walletId = $page.params.walletId;

    // TODO
    async function getWallet(id: string) {
        return {
            "id": id,
            "lorem": "ipsum"
        }
    }

    onMount(async() => {
        wallet = await getWallet(walletId);
    })
</script>

{JSON.stringify(wallet)}






