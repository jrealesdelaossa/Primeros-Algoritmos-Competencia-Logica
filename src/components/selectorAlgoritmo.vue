<template>
  <div class="main">
    <select name="selector" id="selector" v-model="algoritmoSeleccionado">
      <option v-for="p in prices" v-bind:key="p">{{ p }}</option>
    </select>
    {{ algoritmoSeleccionado }}
  </div>
</template>

<script>
export default {
  name: "selectorAlgoritmo",
  data() {
    return {
      prices: ["Suma de dos números", "segundo"],
      algoritmoSeleccionado: "",
    }
  },
}
</script>

<style scoped>

</style>