<script>
    export default {
        props: {
            contenu: String,
            auteur: String,
        }
    }
</script>
<template>
    <p>{{auteur}} : {{contenu}}</p>
</template>