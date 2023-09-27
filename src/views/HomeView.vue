<script setup>
import { onMounted, reactive, ref } from 'vue';
import ListPersonagens from '../components/ListPersonagens.vue';
let personagens = reactive(ref());


onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character?limit=20&offset=0")
    .then(response => response.json())
    .then(response => {
      personagens.value = response.results;
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
            <img src="https://sm.ign.com/ign_br/tv/r/rick-morty/rick-morty_cs71.jpg" class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">Rick And Morty</h5>
              <p class="card-text">Api da serie de animação rick and morty</p>
            </div>
          </div>
        </div>
        <div class="col-sm-12 col-md-6">
          <div class="card">
            <div class="card-body row">
              <ListPersonagens v-for="(person) in personagens"
               :personagemKey="person.id"
               :personagemNome="person.name"
               :personagemStatus="person.name" />
            </div>

          </div>
        </div>
      </div>

    </div>
  </main>
</template>
