<script lang = "ts">
    export let linksToList;
);
</script>

{#each Object.entries(linksToList) as [site, username]}
    <p>{site}: {username}</p>
{/each}