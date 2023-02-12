<template>
  <div class="main">
    <h2>Operación matemática</h2>
    <p>Ingresar dos números enteros, el resultado sera la multiplicación de esos dos números menos el primero</p>

    <div class="entrada">
      <label for="num1">Primer número: </label>
      <input type="number" name="num1" id="num1" v-model="numero1" >
    </div>
    <br>
    <div class="entrada">
      <label for="num2">Segundo número: </label>
      <input type="number" name="num2" id="num2" v-model="numero2" >
    </div>

    <span> = {{ resultado }}</span>

    <div class="boton-calcular">
      <button @click="calcular">Calcular</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "segundoAlgoritmo",
  data() {
    return {
      resultado: 0,
      numero1: 0,
      numero2: 0,
    }
  },
  methods: {
    calcular(){
      this.resultado = (parseInt(this.numero1) * parseInt(this.numero2)) - this.numero1;
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

.boton-calcular {
  margin: 0 24px 24px 24px;
}

.boton-calcular button {
  width: 40%;
  height: 40px;
  border: none;
  border-radius: 12px;
  font-size: 20px;
  text-transform: uppercase;
}

.boton-calcular button:hover {
  scale: 110%;
  cursor: pointer;
}
</style>