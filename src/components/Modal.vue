<script>
import iten from './ListPersonagens.vue'
let personCharacter = "https://rickandmortyapi.com/api/character/";
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
        <div class="modal-body">
            <h2></h2>
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
           @click="" 
           
           >
           Ver detalhes
          </button>
        </div>
      </div>
    </div>
  </div>
</template>