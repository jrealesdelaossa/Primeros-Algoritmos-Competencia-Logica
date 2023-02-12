<template>
  <div class="main">
    <h2>Entrada al cine</h2>
    <p>Ingrese su edad, si es mayor de edad puede pasar, en caso contrario no podría entrar.</p>

    <div class="entrada">
      <label for="age">Su edad: </label>
      <input type="number" name="age" id="age" v-model="age" min="1">
    </div>

    <span> {{ mensaje }}</span>

    <div class="boton-validar">
      <button @click="validar">Validar entrada</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "tercerAlgoritmo",
  data() {
    return {
      mensaje: "",
      age: 1,
    }
  },
  methods: {
    validar() {
      let age = this.age;

      if (age >= 18) {
        this.mensaje = "Usted puede entrar al cine"
      } else {
        this.mensaje = "Usted no puede entrar al cine"
      }
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
  justify-content: space-around;
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
  height: 28px;
  margin: 24px;
  font-size: 24px;
  background-color: #ffffff;
  color: #00af00;
  padding: 12px;
  border: none;
  border-radius: 24px;
}

.boton-validar {
  margin: 0 24px 24px 24px;
}

.boton-validar button {
  width: 60%;
  height: 40px;
  border: none;
  border-radius: 12px;
  font-size: 20px;
  text-transform: uppercase;
}

.boton-validar button:hover {
  scale: 110%;
  cursor: pointer;
}
</style>