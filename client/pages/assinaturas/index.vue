<script setup>
const { data: dataAssinatura } = await useFetch("http://localhost:8000/assinatura/");
console.log(dataAssinatura)
</script>

<template>
<div>
    <h1>assinaturas</h1>
    <NavBar />
    <br/>
    <br/>
    <div v-for="index in dataAssinatura">
    <h1>{{ index.nome }}</h1>
    <h1>{{ index.valor }}</h1>
    <h1>{{ index.id }}</h1>
    </div>
</div>
</template>
