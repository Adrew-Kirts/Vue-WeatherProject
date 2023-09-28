<script>

import { format, render, cancel, register } from 'timeago.js';

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
<!--      <p>Last updated at {{ this.updatedAt.toLocaleDateString() }}</p>-->
      <p>Last updated at {{ format(this.updatedAt) }}</p>
    </div>

</template>

<style scoped>

</style>