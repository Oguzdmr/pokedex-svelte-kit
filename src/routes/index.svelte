<script>
    import {pokemon} from '../stores/pokestore'
    import PokemonCard from '../components/pokemonCard.svelte'
console.log("pokemon",$pokemon);
</script>

<svelte:head>
    <title>Svelte Kit Pokedex</title>
</svelte:head>
<h1>Svelte Kit Pokedex </h1>

<div class="general col-4">
{#each $pokemon as pokeman }

<p> <PokemonCard {pokeman}></PokemonCard></p>
    
{/each}
</div>
<style>
    h1{
        font-size: 8ex;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .general{
        display: grid;
        grid-template-columns: auto auto auto;
    }
</style>