<template>
    <div class="componente">
        <h1>Componente com propriedades assistidas</h1>
        <p>{{ idade }}</p>
        <label>Ano nascimento:</label>
        <input type="number" v-model="anoNascimento" min="1900">
        <label>Ano atual:</label>
        <input type="number" v-model="anoAtual" min="2000">
    </div>
</template>

<script setup>
import { ref } from 'vue';
import { watchEffect } from 'vue';
//import { watch } from 'vue';

const date = new Date();

const anoNascimento = ref(1900)
const anoAtual = ref(date.getFullYear())
const idade = ref(anoAtual.value - anoNascimento.value)

// watch(anoAtual, (ano) => {
//     idade.value = ano - anoNascimento.value
// })

// watch(anoNascimento, (ano) => {
//     idade.value = anoAtual.value - ano
// })

watchEffect(() => {
    idade.value = anoAtual.value - anoNascimento.value
})

</script>

<style scoped>
label{
    margin: 10px;
}
</style>