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

const nome = 'matheus hodecker'
    const idade = 16

    function inverter(texto) {
        return texto.split('').reverse().join('')
    }

    function saudacao() {
        return `Olá, ${nome}!`
    }
    
</script>

<template>



  <div class="info">

  <div class="contador">
  <h1></h1>
  <h1>contador:</h1>
  <h1>{{ contador }}</h1>
  <button @click="acrecentar">increnmentar</button>
  <button @click="decrementar">decrementar</button>
  <button @click="reiniciar">reiniciar</button>
  <div v-if="contador >= 10" class="verde">contador maior que 10</div>
  <div v-else="contador <= 10" class="vermelho">contador menor que 10</div>
</div>

      <h1>Exemplo 1 - Mostrando informações na tela</h1>
      <p>Nome: {{ nome }} </p>
      <p>Idade: {{ idade }}  anos</p>
      <hr />
      <p>Para completar 50 anos faltam: {{ 50 - idade }}  anos</p>
      <p>O nome tem {{ nome.length }}  caracteres</p>
      <p>O nome invertido é: {{ inverter(nome).toUpperCase() }} </p>
      <hr />
      <p> Exemplo de saudação usando função</p>
      <p> {{ saudacao() }}  </p>
  </div>
</template>
<style scoped>
button {
  background-color: chocolate;
  color: white;
  font-weight: bolder;
  border: 5px;
  margin: 2px;
  padding: 20px;
}
.info {
  background-color: rgba(35,12,22,1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
  
}

h1 {
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}
.vermelho{
  border-radius: 10px;
  color: white;
  background-color: red;
  padding: 10px;
  max-width: 200px;
}
.verde{
  border-radius: 10px;
  color: white;
  background-color: green;
  padding: 10px;
  max-width: 200px;
}
.contador{
 border: 10px;
}
</style>
