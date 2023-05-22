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
      appTitle: "La Molisana",
      sectionTitle: "CHI SIAMO",
      productTitle: "LA NOSTRA PASTA",
      productList: [
        "Penne rigate",
        "Linguine",
        "Scialatielli",
        "Mezze maniche"
      ]
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
  <AppHeader :titolo="appTitle" />
  <main>
    <h1>{{ sectionTitle }}</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, aut, consectetur excepturi, porro accusamus
      rem quam est fugiat fuga fugit non nihil. Veritatis dicta repellendus possimus consequuntur aut id vel.</p>
    <ProductList :title="productTitle" :products="productList" />
  </main>
  <AppFooter />
</template>

<style lang="scss">
/* Foglio di stile che contiene selettori da applicare a tutta la pagina, senza scope */
@use './styles/general.scss' as *;
</style>

<style lang="scss" scoped>
/* variabili e mixin che vanno importati solo dove necessario */
@use './styles/partials/_variables.scss' as *;
@use './styles/partials/_mixins.scss' as *;

main {
  background: $themeColor;
  color: white;
  margin-top: 0.5rem;
  padding: 1rem;

  h1 {
    font-weight: 700;
    font-size: 3rem;
  }

}

/* possiamo definirlo nello stlye del componente AppFooter  */
/* inserendolo qui viene comunque ereditato, perchè il footer e' all'interno di app  */
footer {
  background: #CCC;
  padding: 1em;
  text-align: left;
}
</style>