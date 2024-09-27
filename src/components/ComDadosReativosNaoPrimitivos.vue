<template>
    <div class="componente">
        <h1>Componente com dados reativos primitivos</h1>
        <p>Nome: {{ pessoa.nome }} | Idade {{ pessoa.idade }}</p>
        <button @click="fazerAniversario()">Fazer Aniversário</button>
        <button @click="mudarNome()">Mudar Nome</button>
    </div>
</template>

<!-- <script setup>
import { reactive } from "vue"

const pessoa = reactive({ nome: "Alan", idade: 24 })

function fazerAniversario() {
    pessoa.idade++
}

function mudarNome() {
    pessoa.nome = "Alan Nogueira"
}
</script> -->

<!-- options API -->
<script>
export default{
    data:function(){
        return{
            pessoa:{
                nome: "Alan",
                idade: 24
            }
        }
    },
    methods:{
        fazerAniversario:function(){
            this.pessoa.idade++
        },
        mudarNome:function(){
            this.pessoa.nome = "Alan Nogueira"
        }
    }
}
</script>