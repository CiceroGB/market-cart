<template>
  <section class="produtos-container">
    <div v-for="produto in produtos" :key="produto.id">
      <img
        v-if="produtos.foto"
        :src="produtos.foto[0].scr"
        :alt="produtos.foto[0].titulo"
      />
      <p class="preco">{{ produto.preco }}</p>
      <h2 class="titulo">{{ produto.nome }}</h2>
      <p class="preco">{{ produto.descricao }}</p>
    </div>
  </section>
</template>

<script>
import { api } from "@/services.js";

export default {
  name: "ProdutosLista",
  data() {
    return {
      produtos: null,
    };
  },

  methods: {
    getProdutos() {
      api.get("/produto").then((response) => {
        this.produtos = response.data;
      });
    },
  },

  created() {
    this.getProdutos();
  },
};
</script>


<style>
</style>