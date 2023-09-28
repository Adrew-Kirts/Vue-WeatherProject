<script>

export default {
  data(){
    return {
      name: "Ezraville",
      weather: "sunny",
      temperature: 20.55,
      updatedAt: new Date(),

    }
  }
}

</script>

<template>

    <div>
      <h1>Weather in {{ name }}</h1>
      <p>It is currently {{ weather }} with a temperature of {{ temperature }}°C.</p>
      <p>Last updated at {{ updatedAt.toLocaleString() }}</p>
    </div>

</template>

<style scoped>

</style>