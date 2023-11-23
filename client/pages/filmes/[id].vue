<script setup>
const route = useRoute()
console.log(route.params)
const {data: dataFilmes} = await useFetch(`http://127.0.0.1:8000/filmes/${route.params.id}`)
</script>

<template>
    <div>
        <h1>{{ dataFilmes.nome }}</h1><br/>
        <p>{{ dataFilmes.descricao }}</p>
    </div>
</template>