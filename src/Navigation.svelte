<script>
    import { Router, Link} from "svelte-routing";

    export let items = [];
    export let separator = ">";
</script>

<div id="nav">
    <Router>
        <span class="item">
            {#if items && items.length > 0}
                <a href="/">Home</a>
            {:else}
                Home
            {/if}
        </span>
        {#each items as item, i}
            <span>{separator}</span>
            {#if (items.length - 1) === i}
                <span class="item">{item.text}</span>
            {:else}
                <span class="item"><Link to="{item.url}">{item.text}</Link></span>
            {/if}
        {/each}
    </Router>
</div>

<style>
:global(#nav) {
    margin-bottom: 15px;
}
:global(#nav span) {
    margin-left: 0px;
    margin-right: 5px;
}
</style>
