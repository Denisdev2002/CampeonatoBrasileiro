<script setup>
const person = defineProps(["personagemKey","personagemNome","personagemStatus"]);
let imageUrl = "https://rickandmortyapi.com/api/character/avatar/";
let personCharacter = "https://rickandmortyapi.com/api/character/";
</script>

<template>
    <div class="col-4"> 
        <div class="card mb-3">
            <img :src="imageUrl + personagemKey + '.jpeg'" class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title" >{{ person.personagemNome }}</h5>
              <a :href="personCharacter + personagemKey" target="_blank" class="btn btn-primary">Detalhes</a>
            </div>     
        </div>
    </div>
</template>

<style>

</style>
