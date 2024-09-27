<template>
    <div class="componente">
        <h1>Componente com dados reativos primitivos</h1>
        <p>Nome: {{ nome }} | Idade {{ idade }}</p>
        <button v-on:click="fazerAniversario()">Fazer Aniversário</button>
        <button @click="mudarNome()">Mudar Nome</button>
    </div>
</template>

<script setup>
import {ref} from "vue"

const nome = ref("Alan")
const idade = ref(24)

function fazerAniversario(){
    idade.value++
}

function mudarNome(){
    nome.value = "Alan Nogueira"
}
</script>