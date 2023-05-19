<template>
    <footer>
        <!-- Questa immagine usa percorso assoluto quindi il file deve trovarsi nella cartella "public" -->
        <img src="/vite.svg" alt="Vite">
        <span>Realizzato con Vite</span>
    </footer>
</template>

<style scoped>
/* questo stile sovrascrive quello definito nell'app.vue o in style.css */
footer {
    text-align: center;
}

img {
    width: 1rem;
}

span {
    margin-left: 0.5rem;
}
</style>