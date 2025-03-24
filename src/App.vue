<script setup>
import { ref } from 'vue';
const valor = ref(10)

function dupricar() {
  valor.value= valor.value * 2
}
function converter_para_farenheit() {
  temperatura_em_farenheit.value = (temperatura_em_celsius.value)
}
</script>

<template>
 <h1>Olá mundo!</h1>
 <button v-on:click="valor++">incrimentar</button>
 <button v-on:click="valor--">decrementar</button>
 <button v-on:click="dupricar">dupricar</button>
 <p>valor: {{ valor }}</p>
 <hr>
 <h2>conversor de temperatura</h2>
 <input v-model="temperatura_em_celsius" type="number" step="0.1">
 <button v-on:click="converter_para_farenheit">converter</button>
 <p>temperatura em farenheit: </p>
</template>

<style scoped>
button {
  font-weight: bold;
}
</style>
