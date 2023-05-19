<script>
import AppLogo from './AppLogo.vue'

export default {
    name: "AppHeader",
    components: {
        AppLogo
    },
    data() {
        return {
            titolo: "La Molisana"
        }
    },
    mounted() {
        console.log("Caricato il componente Header.");
    }
}
</script>

<template>
    <header>
        <AppLogo />
        <h1>{{ titolo }}</h1>
    </header>
</template>

<style scoped>
/* vale solo per gli header e h1 di questo componente */
header {
    display: flex;
    justify-content: center;
    align-items: center;
}

h1 {
    color: crimson;
    font-size: 4rem;
    margin-left: 1rem;
}
</style>