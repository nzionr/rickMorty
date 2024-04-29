<script setup>
const { name, url, specie, gender, status, location, episodes } = defineProps(["name", "url", "specie", "gender", "status", "location", "episodes"]);
const personagemId = url.split('/')[5];
const imageUrl = "https://rickandmortyapi.com/api/character/avatar/" + personagemId + ".jpeg";
</script>

<template>
  <div class="col-md-4">
    <div class="card p-2 mb-3">
      <img :src="imageUrl" height="280" alt="">
      <p class="text-center">{{ name }}</p>
      <p class="text-center">Espécie: {{ specie }}</p>
      <p class="text-center">Gênero: {{ gender }}</p>
      <p class="text-center">Status: {{ status }}</p>
      <p class="text-center">Localização: {{ location }}</p>
      <p class="text-center">Numéro de Episódio: {{ episodes }}</p>
    </div>
  </div>
</template>

<style>

</style>
