<script setup>
const characterPerson = defineProps(["characterName","characterStatus","characterSpecie","characterGender"]);


</script>
<template>
  <div class="modal-body">
    <p>
      Nome : {{characterName}}
      Status : {{ characterStatus }}
      Specie : {{ characterSpecie }}
      Gender : {{ characterGender }}
    </p>

  </div>


</template>