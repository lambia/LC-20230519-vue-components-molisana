<script>
import AppHeader from './components/AppHeader.vue'
import AppFooter from './components/AppFooter.vue'
import ProductList from './components/ProductList.vue'

export default {
  components: {
    AppHeader,
    AppFooter,
    ProductList
  },
  data() {
    return {
      categoriaProdotti: "LA PASTA"
    }
  },
  methods: {
    logga() {
      console.log("Caricato il componente App, che ha richiamato il metodo 'logga()'");
    }
  },
  mounted() {
    this.logga();
  }
}
</script>

<template>
  <AppHeader />
  <main>
    <h1>I nostri prodotti: {{ categoriaProdotti }}</h1>
    <ProductList />
  </main>
  <AppFooter />
</template>

<style scoped>
main {
  background: crimson;
  color: white;
  margin-top: 0.5rem;
  padding: 1rem;
}

/* possiamo definirlo nello stlye del componente AppFooter  */
/* inserendolo qui viene comunque ereditato, perchè il footer e' all'interno di app  */
footer {
  background: #CCC;
  padding: 1em;
  text-align: left;
}
</style>
