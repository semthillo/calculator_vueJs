<script setup>
import { ref } from 'vue';
import Input from './Input.vue';

const choix = ref("addition");

function faireDeCalcul(){
  switch (choix.value) { 
    case "addition":
      console.log("Addition choisie");
      break;
    case "soustraction":
      console.log("Soustraction choisie");
      break;
    case "multiplication":
      console.log("Multiplication choisie");
      break;
    case "division":
      console.log("Division choisie");
      break;
    default:
      console.log("Aucune opération choisie");
      break;
  }
}

</script>

<template>
<div class="btn-group" role="group" aria-label="Basic checkbox toggle button group">
  <input type="radio" class="btn-check" value="addition" id="btncheck1" autocomplete="off" v-model="choix">
  <label class="btn btn-outline-primary" for="btncheck1">Addition</label>

  <input type="radio" class="btn-check" value="soustraction" id="btncheck2" autocomplete="off" v-model="choix">
  <label class="btn btn-outline-primary" for="btncheck2">Soustraction</label>

  <input type="radio" class="btn-check" value="multiplication" id="btncheck3" autocomplete="off" v-model="choix">
  <label class="btn btn-outline-primary" for="btncheck3">Multiplication</label>

  <input type="radio" class="btn-check" value="division" id="btncheck4" autocomplete="off" v-model="choix">
  <label class="btn btn-outline-primary" for="btncheck4">Division</label>
  
  <button type="button" class="btn btn-dark" @click="faireDeCalcul">Valider</button>
</div>


<Input :choix="choix.value"/>
</template>

<style scoped>
</style>
