<script setup>
import { onMounted, reactive, ref } from 'vue';
import ListTimes from '../components/ListTimes.vue';
let baseUrlSvg = ref("https://raw.githubusercontent.com/PokeApi/sprites/master/sprites/pokemon/other/dream-world/")
let timesCamp = reactive(ref());

onMounted(() =>{
  fetch("https://api.api-futebol.com.br/v1/times/7020")
  // fetch("https://api.api-futebol.com.br/v1/campeonatos/10/?limit=20&offset=0")
  .then(response => response.json())
  .then(response => {
    timesCamp.value = response.results;
    console.log(response);
  })
})
</script>

<template>
  <main>
  <div class="container">
    <div class="row mt-4">
      <div class="col-sm-12 col-md-6">
        <div class="card" style="width: 18rem;">
          <img src="https://cdn.api-futebol.com.br/escudos/638d3487aa471.svg" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">Card title</h5>
            <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
            <a href="#" class="btn btn-primary">Detalhes</a>
          </div>
        </div>
      </div>
      <div class="col-sm-12 col-md-6">
        <div class="card">
          <div class="card-body row">
        <ListTimes
        v-for="time in timesCamp"
        :key="time_id.id"
        :nomepop="nome_popular.name"
        :sigla="sigla.sigla"
        :escudo="escudo.escudo"
        :nome="nome.nome"
        :apelido="apelido.apelido"
        
        
        />
      </div>
        </div>
          </div>
    </div>
  </div>
  </main>
</template>
