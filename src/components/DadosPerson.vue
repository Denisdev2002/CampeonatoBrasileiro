<script setup>
const characterPerson = defineProps(["characterName","characterStatus","characterSpecie","characterGender"]);


</script>
<template>
  <div class="modal-body">
    <p>
      Nome : {{characterName}} <br>
      Status : {{ characterStatus }} <br>
      Specie : {{ characterSpecie }} <br>
      Gender : {{ characterGender }} <br>
    </p>

  </div>


</template>