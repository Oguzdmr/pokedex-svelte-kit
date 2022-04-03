<script>
    import {pokemon} from '../stores/pokestore'
    import PokemonCard from '../components/pokemonCard.svelte'

    let searchTerm = "";
    let filteredPokemon = [];

    $:{
        if(searchTerm){
            filteredPokemon = $pokemon.filter(pokeman => pokeman.name.toLowerCase().includes(searchTerm.toLowerCase()))
        }else{
            filteredPokemon = [...$pokemon]
        }
    }
</script>

<svelte:head>
    <title>Svelte Kit Pokedex</title>
</svelte:head>
<h1>Svelte Kit Pokedex </h1>

<input class="search" type="text" bind:value={searchTerm} placeholder="Search Pokemon">

<div class="general col-4">
{#each filteredPokemon as pokeman }

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
        grid-template-columns: auto auto;
    }
    .search{
        width: 100%;
        border-radius: 5px;
        border-width: 2px;
        font-size: 1.25rem;
        line-height: 1.75rem;
        padding: 4px;
        opacity: 1;
    }
</style>