<script setup>

import { livros } from '@/_data/livros.js'
import {adicionarAoCarrinho } from '@/_data/carrinho.js'
import Cardlivro from './Cardlivro.vue';

</script>
<template>
<div class="listagem-livros">
    <Cardlivro v-for="livro in livros" :key="livro.id" :livro="livro" 
    @adicionarAoCarrinho="adicionarAoCarrinho" />
   </div>
 </template>
 
<style scoped>
.listagem-livros {
  display: flex;
  flex-wrap: wrap;
}

</style>