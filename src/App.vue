<!-- eslint-disable prettier/prettier -->
<script setup>


const show = true
const array = [1,2,3,4,5,6,7,8,9,10]

</script>

<template>
  <div class="col-6">
    <h2>Composition</h2>
    <!--INICIO V-IF, V-ELSE-IF, V-ELSE -->
    <span v-if="show">V-IF</span>
    <span
      v-else-if="show
        == null"
    >V-ELSE-IF</span>
    <span v-else>V-Else</span>
    <!--FIM V-IF, V-ELSE-IF, V-ELSE -->
    <br>
    <!--INICIO V-SHOW -->
    <span v-show="show">Falando sobre o V-Show</span>
    <!--INICIO V-SHOW -->
    <br>
    <!--INICIO V-FOR -->
    <ul>
      <li
        v-for="item, index in array"
        :key="index"
      >
        {{ item }}
      </li>
    </ul>
    <!--FIM V-FOR -->
  </div>
</template>

<style>
</style>

<!-- Diferenças do v-if para o v-show
O v-if, se a condição não for satisfeita, não renderiza, o que torne mais seguro
O v-show, com a condição satisfatoria ou não, apresenta no HTML, mas não renderiza o resultado, mais parecido com o CSS display: none-->