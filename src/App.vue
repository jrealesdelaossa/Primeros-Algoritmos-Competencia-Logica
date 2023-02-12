<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Hola mundo"/> -->
    <div class="cabecera">
      <label class="text-selector" for="selector">Seleccione el algoritmo que desea revisar</label>
      <select class="selector-opciones" name="selector" id="selector" v-model="algoritmoSeleccionado" @change="seleccionar">
        <option v-for="p in algoritmos" v-bind:key="p">{{ p }}</option>
      </select>
    </div>

    <div v-if="primero" class="show-algoritmo">
      <primer-algoritmo />
    </div>
    <div v-if="segundo" class="show-algoritmo">
      <segundo-algoritmo />
    </div>
    <div v-if="tercero" class="show-algoritmo">
      <tercer-algoritmo />
    </div>
    <div v-if="cuarto" class="show-algoritmo">
      <cuarto-algoritmo />
    </div>
    <br>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import PrimerAlgoritmo from "@/components/primerAlgoritmo.vue";
import SegundoAlgoritmo from "@/components/segundoAlgoritmo.vue";
import TercerAlgoritmo from "@/components/tercerAlgoritmo.vue";
import CuartoAlgoritmo from "@/components/cuartoAlgoritmo.vue";
export default {
  name: 'App',
  components: {
    CuartoAlgoritmo,
    TercerAlgoritmo,
    SegundoAlgoritmo,
    PrimerAlgoritmo,
    // HelloWorld
  },
  data() {
    return {
      algoritmos: [
          "Suma de dos números",
          "Operación matemática",
          "Entrada al cine",
          "Número mayor"
      ],
      algoritmoSeleccionado: "",
      primero: undefined,
      segundo: undefined,
      tercero: undefined,
      cuarto: undefined,
    }
  },
  methods: {
    seleccionar() {
      if (this.algoritmoSeleccionado === "Suma de dos números") {
        this.primero = true;

        this.segundo = false;
        this.tercero = false;
        this.cuarto  = false;
      } else if (this.algoritmoSeleccionado === "Operación matemática") {
        this.segundo = true;

        this.primero = false;
        this.tercero = false;
        this.cuarto  = false;
      } else if (this.algoritmoSeleccionado === "Entrada al cine") {
        this.tercero = true;

        this.primero = false;
        this.segundo = false;
        this.cuarto  = false;
      } else if (this.algoritmoSeleccionado === "Número mayor") {
        this.cuarto = true;

        this.primero = false;
        this.segundo = false;
        this.tercero = false;
      } else {
        this.primero = false;
        this.segundo = false;
        this.tercero = false;
        this.cuarto  = false;
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
