<script setup>
const {data: dataUser} = await useFetch("http://127.0.0.1:8000/usuarios/")
console.log(dataUser.nome)
</script>

<template>
    <div>
        <h1>usuarios</h1>
        <NavBar/>
        <div v-for="index in dataUser">
            <NuxtLink :to="`/usuarios/${index.id}`"><h1>{{ index.nome }}</h1></NuxtLink>
        </div>
    </div>
</template>