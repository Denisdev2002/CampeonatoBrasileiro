<script>
import { onMounted, reactive, ref } from 'vue';
let character = reactive(ref());
onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character?limit=20&offset=0")
    .then(response => response.json())
    .then(response => {
      character.value = response.results;
      console.log(response);
    })
})
// let personCharacter = "https://rickandmortyapi.com/api/character/";
</script>
<template>
<!-- Modal -->
<div class="modal fade"
 id="modelPopup"
 tabindex="-1"
 aria-labelledby="exampleModalLabel"
 aria-hidden="true">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h1 class="modal-title fs-5" id="exampleModalLabel">Detalhes</h1>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body" >  
          <p>
              Nome : <br>
              Status : <br>
              Especie : <br>
              Gênero : <br>


            </p>   
        </div>
        <div class="modal-footer">
          <button 
            type="button"
            class="btn btn-secondary"
            data-bs-dismiss="modal"
            @click="close()"
            >
            Fechar
          </button>
  
          <button
           type="button"
           class="btn btn-primary" 
           >
           Ver detalhes
          </button>
          
        </div>
      </div>
    </div>
  </div>
</template>