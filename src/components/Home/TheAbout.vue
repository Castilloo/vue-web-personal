<template>
    <div>
        <div class="about">
            <div class="about__content">
                <div class="about__content__left">
                    <img
                        class="about__content__left__img" 
                        src="../../assets/luffy.jpg" 
                    >
                </div>
                <div class="about__content__right">
                    <h3 class="about__content__right__title">Sobre mi</h3>
                    <p class="about__content__right__text">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Laudantium corporis fuga delectus nisi minus, aliquam est.
                    </p>
                    <div class="about__content__right__ctrls">
                        <v-button-main 
                        texto="LinkedIn"
                        color-texto="#ff9f2a"
                        color-fondo="#212121" 
                        />
                        <v-button-main 
                            texto="Github"
                            color-texto="#212121"
                            color-fondo="#ff9f2a" 
                        />      
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
        import VButtonMain from '../base/VButtonMain.vue';

    export default {
        name: 'TheAbout',
        components: {
            VButtonMain
        }
    }
</script>

<style lang="scss" scoped>
    @import '../app';

    .about {
        display: flex;
        justify-content: center;
        align-items: center;
        background: $color1;
        opacity: 0.95;
        &__content {
            width: 50%;
            padding: 5em 0;
            display: flex;
            justify-content: center;
            align-items: center;
            &__left {
                border: 1px solid $color2;
                width: 150px;
                height: 200px;
                margin-right: 3em;
                &__img {
                    width: 100%;
                    height: 100%;
                    position: relative;
                    left: 20px;
                    bottom: 20px;
                }
            }
            &__right {
                display: block;
                width: 50%;
                color: $color-white;
                &__title{
                    font-family: $ff-primary;
                    font-size: 20px;
                    border-bottom: 1px solid $color2;
                    padding-bottom: 1em;
                    margin-bottom: 1em;
                }
                &__text {
                    font-size: 15px;
                    font-family: $ff-secondary;
                    margin-bottom: 1.5em;
                }
            }
        }
    }
    
</style>