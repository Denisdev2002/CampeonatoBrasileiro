<script setup>
const timesCamp = defineProps(["nomepop","sigla","escudo","nome","apelido"]);

</script>

<template>
    <div class="col-4"> 
        <div class="card mb-3">
            <!-- <img src="https://cdn.api-futebol.com.br/escudos/638d3487aa471.svg" class="card-img-top" alt="..."> -->
            <img :src="timesCamp.escudo" class="card-img-top" alt="...">

            <div class="card-body">
              <h5 class="card-title">{{ timesCamp.nomepop }}</h5>
              <a :href="timesCamp.sigla" target="_blank" class="btn btn-primary">Detalhes</a>
            </div>     
        </div>
    </div>
</template>

<style>

</style>
