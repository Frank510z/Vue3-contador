<!-- Template - HTML-->
<template>
  <div class="contenedor">
    <h1>{{ mensaje }}</h1>
    <img src="./assets/logo.svg" alt="" height="200px" />

    <hr />

    <h2>Contador: {{ contador }}</h2>
    <button @click="inclementar()">+1</button>
    <button @click="disminuir()">-1</button>
    <button @click="reset()">Reset</button>
  </div>
</template>

<!-- script - JavaScript-->
<script>
export default {
  data: () => ({
    contador: 0,
    mensaje: "Hola Mundo",
  }),

  methods: {
    inclementar() {
      this.contador++;
    },

    disminuir() {
      this.contador--;
    },

    reset() {
      this.contador = 0;
    },

  },
};
</script>

<!-- Style - CSS-->
<style scoped>
h1 {
  color: red;
  font-size: 3rem;
}

.contenedor {
  text-align: center;
}

h2 {
  font-size: 2rem;
}

button {
  padding: 17px 40px;
  border-radius: 10px;
  border: 0;
  margin: 0 6px;
  background-color: #32475c;
  letter-spacing: 1.5px;
  font-size: 15px;
  transition: all 0.3s ease;
  box-shadow: #40b27f 0px 10px 0px 0px;
  color: hsl(0, 0%, 100%);
  cursor: pointer;
}

button:hover {
  box-shadow: #ffe600 0px 7px 0px 0px;
}

button:active {
  transform: translateY(5px);
  transition: 200ms;
  color: #ffe600;
}
</style>
