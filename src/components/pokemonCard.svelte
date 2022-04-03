<script>
    export let pokeman;
</script>

    <a href={`/pokeman/${pokeman.id}`}>
        <img src={pokeman.image} alt={pokeman.name}>
        <h2>{pokeman.id}.  {pokeman.name}</h2>
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
    }

</style>