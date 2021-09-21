<template>
  <section>
    <h1>Compre ou Venda</h1>
    <ProdutosBuscar />
    <ProdutosLista />
  </section>
</template>

<script>
import ProdutosLista from "@/components/ProdutosLista.vue";
import ProdutosBuscar from "@/components/ProdutosBuscar.vue";

export default {
  name: "Home",
  components: {
    ProdutosBuscar,
    ProdutosLista,
  },
};
</script>
