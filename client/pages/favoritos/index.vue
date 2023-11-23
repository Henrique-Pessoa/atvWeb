<script setup>
const {data: dataFavorito} = await useFetch("http://127.0.0.1:8000/favoritos/");

</script>

<template>
    <div>
        <h1>favoritos</h1>
        <NavBar/>
        <div v-for="index in dataFavorito">{{ index.idFilmeFK.nome }}</div>
    </div>
</template>