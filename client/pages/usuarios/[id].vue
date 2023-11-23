<script setup>
    const route = useRoute()
    const {data: dataFav} = await useFetch(`http://127.0.0.1:8000/favoritos/${route.params.id}`)

</script>

<template>
<div>
    <div v-for="index in dataFav.idFilmeFK">
        <h1>{{ index }}</h1>
    </div>
    <section>
    <input  v-model="nome">
    <input  v-model="descricao">
    <input  v-model="foto">
    <input  v-model="banner">
    <input  v-model="logo">
    <input  v-model="idCategoriaFK">
    <button @click="sendForm">Enviar</button>
</section>
</div>
</template>