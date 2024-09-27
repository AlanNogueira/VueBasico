<template>
    <div class="componente">
        <h1>Componente que escuta evento</h1>
        <p1>Total: R${{ total }}</p1>
        <div class="lista">
            <EmiteEvento item="item1" :preco="1.00" @foi-adicionado="atualizarTotal"/>
            <EmiteEvento item="item2" :preco="5.00" @foi-adicionado="atualizarTotal"/>
            <EmiteEvento item="item3" :preco="10.00" @foi-adicionado="atualizarTotal"/>
        </div>
    </div>
</template>

<script setup>
import EmiteEvento from './EmiteEvento.vue';
import {ref} from 'vue'
const total = ref(0)

function atualizarTotal(p){
    const valor = total.value + p
    total.value = +valor.toFixed(2)
}
</script>

<style scoped>
.lista {
    display: flex;
    justify-content: space-between;
}
</style>