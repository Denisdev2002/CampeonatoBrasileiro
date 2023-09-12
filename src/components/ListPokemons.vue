<script setup>
const pokemon = defineProps(["name","url"]);

</script>

<template>
    <div class="col-4"> 
        <div class="card mb-3">
            <img src="https://assets.pokemon.com/assets/cms2/img/pokedex/full/001.png" class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">{{ pokemon.name }}</h5>
              <a :href="pokemon.url" target="_blank" class="btn btn-primary">Detalhes</a>
            </div>     
        </div>
    </div>
</template>

<style>

</style>
