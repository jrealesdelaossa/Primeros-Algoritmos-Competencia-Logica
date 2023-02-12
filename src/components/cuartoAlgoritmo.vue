<template>
  <div class="main">
    <h2>Número mayor</h2>
    <p>Digite tres números enteros, <strong>diferentes</strong> entre si. El algoritmo retornara el número mayor.</p>

    <div class="entrada">
      <label for="num1">Primer número: </label>
      <input type="number" name="num1" id="num1" v-model="numero1" >
    </div>
    <br>
    <div class="entrada">
      <label for="num2">Segundo número: </label>
      <input type="number" name="num2" id="num2" v-model="numero2" >
    </div>
    <br>
    <div class="entrada">
      <label for="num3">Tercer número: </label>
      <input type="number" name="num3" id="num3" v-model="numero3" >
    </div>

    <p class="text">El número mayor es: </p>
    <span>{{ resultado }}</span>

    <div class="boton-calcular">
      <button @click="calcular">Calcular</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "cuartoAlgoritmo",
  data() {
    return {
      mayor: 0,
      numero1: 0,
      numero2: 0,
      numero3: 0,
      resultado: "",
    }
  },
  methods: {
    calcular(){
      let num1 = this.numero1;
      let num2 = this.numero2;
      let num3 = this.numero3;

      if (num1 !== num2 && num1 !== num3 && num2 !== num3) {
        if (num1 > num2) {
          if (num1 > num3) {
            this.mayor = num1;
          } else {
            this.mayor = num3;
          }
        } else {
          if (num2 > num3) {
            this.mayor = num2;
          } else {
            this.mayor = num3;
          }
        }

        this.resultado = `El número mayor es ${this.mayor}`;
      } else {
        this.resultado = "Por favor, números diferentes";
      }
    },

    resetear() {
      this.resultado = 0;
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

.text {
  margin: 24px 0 0 0;
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
  font-size: 20px;
  background-color: #ffffff;
  color: #00af00;
  padding: 12px;
  border: none;
  border-radius: 24px;
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