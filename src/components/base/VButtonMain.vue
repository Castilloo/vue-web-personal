<template>
    <a 
        href="#" 
        class="main-btn"
        :style="{ background: colorFondo, color: colorTexto }"   
    >
        {{ texto }}
    </a>
</template>

<script>
    export default {
        name: 'VButtonMain',
        props: {
            texto: String,
            colorTexto: String,
            colorFondo: String
        }
    }
</script>

<style lang="scss" scoped>
    @import '../app';
    .main-btn {
        padding: 7px 20px;
        font-family: $ff-secondary;
        border: 1px solid;
        margin: 5px;
        text-decoration: none;
    }
</style>