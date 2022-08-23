<!-- eslint-disable prettier/prettier -->
<script setup>
import { ref, reactive, onMounted } from 'vue'

const nome = ref('Bill'); // ref = usado normalmente em dados primitivos, ex. string

const person = reactive({ // utilizado normalmente em objetos
    name: 'Bianchi',
    age: 37,
    job: 'Dev',
})


onMounted(()=>{ // reactive
    person.name = 'Teste de nome'
    console.log(person)
})


</script>

<template>
  <h2>Composition</h2>
  <p>{{ nome }}</p>
  <input
    v-model="nome"
    type="text"
  > <!-- usando ref -->
  <hr>
  <p>{{ person.name }}</p> <!-- usando reactive-->
</template>

<style scoped>
</style>
