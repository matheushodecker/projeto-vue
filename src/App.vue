<script setup>
import { ref } from 'vue';

const contador = ref(0);
function decrementar(){
  if(contador.value > 0){

  contador.value--;
}}


function acrecentar(){

    contador.value++;
  
}
function reiniciar(){

  contador.value = 0;

}

</script>

<template>
  <button @click="acrecentar">+</button>
  <button @click="decrementar">-</button>
  <button @click="reiniciar"></button>
  <p>valor do contador: {{ contador }}</p>
 
</template>

<style scoped>
button {
  background-color: chocolate;
  color: white;
  font-weight: bolder;
  border: 0;
  margin: 2px;
  padding: 20px;
}
</style>
