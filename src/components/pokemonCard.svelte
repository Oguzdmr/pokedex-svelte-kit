<script>
    export let pokeman;
</script>

    <a href={`/pokeman/${pokeman.id}`}>
        <img src={pokeman.image} alt={pokeman.name}>
        <h2>{pokeman.id}.  {pokeman.name.toUpperCase()}</h2>
    </a>


<style>
    a{ 
        display: flex;
        align-items: center;
        flex-direction: column;
        background-color: rgb(228, 228, 228);
        text-decoration: none;
        color: rgb(57, 56, 56);
        margin: 20px;
        box-shadow: 0 1px 2px 0 rgb(0 0 0 / 0.05);
    }
    a:hover{
        box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
    }

</style>