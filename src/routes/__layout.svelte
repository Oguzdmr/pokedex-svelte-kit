<script>
    import Nav from "../components/nav.svelte"
</script>
<div class="general">
<Nav></Nav>
<slot></slot>
</div>

<style>
    .general{
        padding: 8px;
        margin: auto;
        max-width: 1000px;
    }
</style>
