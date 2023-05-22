<script>
export default {
    name: "ProductList",
    props: {
        title: String,
        products: Array
    },
    data() {
        return {

        }
    },
    mounted() {
        //Questo darebbe un warning, non è possibile mutare dati nelle props
        // this.title = "Nuovo Titolo Aggiornato";
    }
}
</script>

<template>
    <div>
        <h3>{{ title }}</h3>
        <ul>
            <li v-for="product in products">{{ product }}</li>
        </ul>
    </div>
</template>

<style scoped lang="scss">
div {
    margin-top: 2rem;
}

ul {
    list-style-type: none;
    margin-top: 0.5rem;
}
</style>