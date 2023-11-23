<script setup>
const {data:dataFilme} = await useFetch("http://127.0.0.1:8000/filmes/")

</script>

<template>
    <div>
        <h1>filmes</h1>
        <NavBar/>
        <div v-for="index in dataFilme">
        <h1>{{ index.nome }}</h1>
        <NuxtLink :to="`/filmes/${index.id}`"> <img :src="`http://127.0.0.1:8000${index.banner}`"/></NuxtLink>
        </div>
    </div>
</template>