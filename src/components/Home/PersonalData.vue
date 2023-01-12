<template>
    <div class="personal-data">
        <div class="personal-data__left">
            <div class="personal-data__left__content">
                <span class="personal-data__left__content__text">Hola</span>
                <h3 class="personal-data__left__content__name">Soy Luffy</h3>
                <p class="personal-data__left__content__description">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque aut aperiam praesentium quas magnam libero maiores et sequi dignissimos, atque omnis labore voluptatibus impedit quidem distinctio fugit nemo molestias nostrum!
                </p>
                <!-- En los comentarios se usan cuando en el script se importan las variables de los colores en sass, pero por problemas en la configuyarión no se pueden visualizar esas variables -->
                <!-- <v-button-main
                    texto="Contactar"
                    :color-texto="color2"
                    :color-fondo="color1"
                /> -->
                <v-button-main
                    texto="Contactar"
                    color-texto="#ff9f2a"
                    color-fondo="#212121"
                />
            </div>
        </div>
        <div class="personal-data__right">
            <img
                class="personal-data__right__img"
                src="@/assets/luff.png"
                alt="">
        </div>
    </div>
</template>

<script>
    import VButtonMain from '../base/VButtonMain.vue';
    // import { colorone, colortwo } from '../_app.scss';

    // console.log(colorone)

    export default {
        name: 'PersonalData',
        // data() {
        //     return {
        //         color1: colorone,
        //         color2: colortwo
        //     }
        // },
        components: {
            VButtonMain
        }
    }
</script>

<style lang="scss" scoped>
    @import '../app';

    .personal-data{
        display: flex;
        &__left {
            background: $color1;
            width: 60%;
            display: flex;
            justify-content: center;
            align-items: center;
            &__content {
                width: 350px;
                color: $color-white;
                &__text {
                    font-family: $ff-secondary;
                    font-size: 14px;
                    margin-bottom: 10px;
                }
                &__name {
                    font-family: $ff-primary;
                    font-size: 24px;
                    color: $color2;
                    margin-bottom: 10px;
                }
                &__description {
                    font-family: $ff-secondary;
                    font-size: 20px;
                    margin-bottom: 2em;
                }
            }
        }

        &__right {
            background: $color2;
            width: 40%;
            &__img {
                width: 200px;
                position: relative;
                right: 100px;
            }
        }
    }
</style>