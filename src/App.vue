<script setup>
//ref() cria dados reativos, para acessar esses dados precisamos usar o .value
import {ref} from "vue";
//variavel inicial
const numero = ref(0);
//funcao para aumentar
function aumentar(){ 
    numero.value ++
}

//funcao para diminuir
function diminuir(){
    if(numero.value > 0){
        numero.value --
    }
}

</script>

<template>
    <h1>Contador</h1>
    <h2>{{ numero }}</h2>
    <button @click="aumentar">+</button>
    <button @click="diminuir">-</button>

</template>

<style scoped lang="scss">

</style>
