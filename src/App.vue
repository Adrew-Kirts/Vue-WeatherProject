<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import city from "@/components/City.vue";
import citiesList from "@/views/CitiesList.vue";
// import CitiesList from "@/views/CitiesList.vue";

// Ajoutez dans votre composant App la méthode `onListClick` qui se contentera pour l'instant de faire une [alerte]
// (https://developer.mozilla.org/fr/docs/Web/API/Window/alert) pour marquer le fait qu'un utilisateur a cliqué dessus.
function onListClick() {
  alert("this is an alert")
}

</script>

<template>
  <header>
    <div class="wrapper">
      <HelloWorld msg="Weather near you" />
      <nav>
          <RouterLink to="/">Home</RouterLink>
          <RouterLink to="/ville">Weather</RouterLink>

          <button @click="onListClick">ALERT</button><br><br>
      </nav>
    </div>
  </header>

  <RouterView />

    <router-link to="/villes">Villes</router-link>


    <div>
      <city v-for="city in citiesList.data().cities" :key="city.id" :name="city.name" :weather="city.weather"
            :temperature="city.temperature" :updatedAt="city.updatedAt" />
    </div>


</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
