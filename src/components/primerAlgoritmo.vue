<template>
  <div class="main">
    <h2>Suma de dos números</h2>
    <p>Realizar la suma de dos números enteros</p>

    <div class="entrada">
      <label for="num1">Primer número: </label>
      <input type="number" name="num1" id="num1" v-model="numero1" @change="add">
    </div>
    <p class="suma">+</p>
    <div class="entrada">
      <label for="num2">Segundo número: </label>
      <input type="number" name="num2" id="num2" v-model="numero2" @change="add">
    </div>
    <span> = {{ resultado }}</span>
  </div>
</template>

<script>
export default {
  name: "primerAlgoritmo",
  data() {
    return {
      resultado: 0,
      numero1: 0,
      numero2: 0,
    }
  },
  methods: {
    add(){
      this.resultado = parseInt(this.numero1) + parseInt(this.numero2);
    }
  }
}
</script>


<style scoped>
.main {
  display: flex;
  flex-direction: column;
  width: 400px;
  background-color: #00af00;
  border: 12px solid #FFF;
  border-radius: 24px;
  color: #FFFFFF;
}

.entrada {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 0 40px;
}

h2 {
  text-transform: uppercase;
}

.suma {
  text-align: center;
  font-size: 40px;
  margin: 0 0 0 140px;
}

input {
  border: none;
  background: #cdefcd;
  color: #000000;
  /* font-size: 16px; */
  text-align: center;
  /* width: 80px; */
  border-radius: 4px;
}

span {
  margin: 24px;
  font-size: 50px;
}
</style>