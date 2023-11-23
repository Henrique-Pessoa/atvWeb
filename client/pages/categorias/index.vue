<script setup>
    const { data: dataCategoria } = await useFetch("http://127.0.0.1:8000/categoria/");

</script>

<template>
    <div>
        <h1>categorias</h1>
        <NavBar/>
        <div v-for="index in dataCategoria">
        <h1>{{ index.nome }}</h1>
        </div>
    </div>
</template>