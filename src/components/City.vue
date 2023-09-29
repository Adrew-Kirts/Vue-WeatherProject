<script>

import { format } from 'timeago.js';

// export default {
//   data(){
//     return {
//       name: "Ezraville",
//       weather: "sunny",
//       temperature: 20.55,
//       updatedAt: new Date(),
//     }
//   }
// }

export default {
  name: "City.vue",
  methods: {format},
  props: {
    name: String,
    weather: String,
    temperature: Number,
    updatedAt: Date
  }
}

</script>

<template>

    <div>
      <h1>Weather in {{ this.name }}</h1>
      <p>It is currently {{ this.weather }} with a temperature of {{ this.temperature }}°C.</p>
      <p>Last updated {{ format(this.updatedAt) }}</p>
    </div>

</template>

<style scoped>

</style>