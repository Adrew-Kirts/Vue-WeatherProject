<script>

import city from "@/components/City.vue";

export default {
  computed: {
    city() {
      return city
    }
  },
  data(){
    return {

      cities: [
        {
          id: 1,
          name: 'Ville 1',
          weather: 'Ensoleillé',
          temperature: 22.0,
          updatedAt: new Date()
        },
        {
          id: 2,
          name: 'Ville 2',
          weather: 'Peu nuageux',
          temperature: 19.5,
          updatedAt: new Date()
        }
      ]
    }
  }
}


</script>

<template>


<!--  <div class="citiesList">-->
<!--    <h1>Météo - Liste des villes</h1>-->
<!--  </div>-->


<!--  <component :is="city"></component>-->

<!--      <div>-->
<!--        <h1>Weather in {{ cities[0].name }}</h1>-->
<!--        <p>It is currently {{ cities[0].weather }} with a temperature of {{ cities[0].temperature }}°C.</p>-->
<!--        <p>Last updated at {{ cities[0].updatedAt }}</p>-->
<!--      </div>-->

<!--  <div>-->
<!--    <h1>Weather in {{ cities[0].name }}</h1>-->
<!--    <p>It is currently {{ cities[0].weather() }} with a temperature of {{ city.props.temperature() }}°C.</p>-->
<!--    <p>Last updated at {{ cities[0].updatedAt().toLocaleString() }}</p>-->
<!--  </div>-->

</template>

<style scoped>

</style>