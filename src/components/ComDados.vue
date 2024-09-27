<template>
    <div class="componente">
        <h1>Componente com dados</h1>
        <p1>Nome: {{ nomeProduto }} - {{ codigoProduto }}</p1>
    </div>
</template>

<style scoped>
</style>

<script setup>
    const nomeProduto = "Apontador"
    const codigoProduto = "#987"
</script>

<!-- <script>
//option API
// export default{
//     data:function(){
//         return{
//             nomeProduto: "Caderno",
//             codigoProduto: "#321"
//         }
//     }
// }

//composition API
export default{
    setup:function(){
        const nomeProduto = "Lápis"
        const codigoProduto = "#789"
        return{nomeProduto, codigoProduto}
    }
}
</script> -->