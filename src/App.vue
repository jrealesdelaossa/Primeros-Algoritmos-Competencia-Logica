<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Hola mundo"/> -->
    <primer-algoritmo />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import PrimerAlgoritmo from "@/components/primerAlgoritmo.vue";

export default {
  name: 'App',
  components: {
    PrimerAlgoritmo,
    // HelloWorld
  }
}
</script>

<style>
body {
  background-color: #cdefcd;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

}
</style>
