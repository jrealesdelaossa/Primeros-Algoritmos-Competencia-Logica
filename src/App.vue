<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Hola mundo"/> -->
    <div class="cabecera">
      <label class="text-selector" for="selector">Seleccione el algoritmo que desea revisar</label>
      <select class="selector-opciones" name="selector" id="selector" v-model="algoritmoSeleccionado" @change="seleccionar">
        <option v-for="p in prices" v-bind:key="p">{{ p }}</option>
      </select>
    </div>

    <div v-if="primero" class="show-algoritmo">
      <primer-algoritmo />
    </div>
    <br>
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
  },
  data() {
    return {
      prices: ["Suma de dos números", "segundo"],
      algoritmoSeleccionado: "",
      primero: undefined,
      segundo: undefined,
    }
  },
  methods: {
    seleccionar() {
      if (this.algoritmoSeleccionado === "Suma de dos números") {
        this.primero = true;
      } else {
        this.primero = false;
      }
    }
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

.cabecera {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  height: 40px;
}

.text-selector {
  font-size: 24px;
}

.selector-opciones {
  margin-left: 24px;
  width: 400px;
  height: 40px;
  font-size: 16px;
  border: 4px solid #00af00;
  border-radius: 12px;
}

.show-algoritmo {
  display: grid;
  place-content: center;
  margin-top: 40px;
}
</style>
