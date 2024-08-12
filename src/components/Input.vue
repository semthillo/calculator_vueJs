<script setup>
const props = defineProps(['choix'])
</script>

<template>
<div class="input-group add champ" v-if="choix === 'addition'">
  <span class="input-group-text">Entrez Les Valeurs</span>
  <input type="number" aria-label="First name" class="form-control">
  <input type="number" aria-label="Last name" class="form-control">
</div>
</template>

<style scoped>
</style>
