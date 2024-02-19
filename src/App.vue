<script setup>
import { ref } from 'vue';

const contador = ref(0)
function decrementar(){
  contador.value--
}
function acrecentar(){
  contador.value++
}


</script>

<template>
  <button @click="acrecentar">+</button>
  <button @click="decrementar">-</button>
  <p>valor do contador: {{ contador }}</p>
</template>

<style scoped></style>
