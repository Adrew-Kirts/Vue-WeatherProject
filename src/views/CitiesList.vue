<script setup>

import city from "@/components/City.vue";

</script>

<template>

  <div class="citiesList">
    <h1>Météo - Liste des villes</h1>
  </div>


  <component :is="city"></component>

      <div>
        <h1>Weather in {{ city.props.name() }}</h1>
        <p>It is currently {{ city.props.weather() }} with a temperature of {{ city.props.temperature() }}°C.</p>
        <p>Last updated at {{ city.props.updatedAt().toLocaleString() }}</p>
      </div>

</template>

<style scoped>

</style>