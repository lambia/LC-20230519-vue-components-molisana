<script>
import AppLogo from './AppLogo.vue'

export default {
    name: "AppHeader",
    props: {
        titolo: String
    },
    components: {
        AppLogo
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

<style scoped lang="scss">
/* variabili e mixin vanno importati solo dove necessario */
@use '../styles/partials/_variables.scss' as *;
@use '../styles/partials/_mixins.scss' as *;

/* vale solo per gli header e h1 di questo componente */
header {
    /***** MIXIN ****/
    /* Attenzione, il mixin del Justify applica già il display flex */
    /* Riporto entrambi solo per mostrarvi come si usano, ma si può semplificare ;) */
    @include display-flex;
    @include justify("center");

    align-items: center;
}

h1 {
    color: $themeColor;
    font-size: 4rem;
    margin-left: 1rem;
}
</style>