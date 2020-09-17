<template>
  <div id="app" class="container-fluid">
    <h1 class="text-center pb-5">Disponible en streaming</h1>
    <Movies msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import Movies from './components/Movies.vue'

export default {
  name: 'App',
  components: {
    Movies
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 60px;
}
</style>
