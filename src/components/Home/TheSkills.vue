<template>
    <div class="skills">
        <h3 class="skills__title">Mis habilidades</h3>
        <p class="skills__text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat sit dolorem magnam eius libero, illo ipsa esse quas odio, totam excepturi. Mollitia aliquid molestiae nostrum obcaecati quo, perspiciatis labore quam.</p>
        <div class="skills__items">
            <div 
                class="skills__item"
                v-for="habilidad in habilidades"
                :key="habilidad.id"
            >
                <v-card-main 
                    :titulo="habilidad.titulo"
                    :contenido="habilidad.contenido"
                    :color="habilidad.color"
                />
            </div>
        </div>
    </div>
</template>

<script>
    // import { colortwo, colorthree, colorfour, colorfive } from '@/components/_app.scss'
    import VCardMain from '../base/VCardMain.vue';

    export default {
        name: 'TheSkills',
        data() {
            return {
                habilidades: [{
                    'id': 0, 
                    titulo: 'Gomu Gomu', 
                    contenido: 'Comió la fruta Gomu Gomu y el cuerpo de Luffy se convirtió en goma',
                    color: '#ff9f2a'
                },{
                    'id': 1, 
                    titulo: 'Super fuerza', 
                    contenido: 'Posee una fuerza descomunarl y genera grandes impactos con la elasticidad de sus extremidaded y puede cargar mucho peso',
                    color: '#18dcff'
                },{
                    'id': 2, 
                    titulo: 'Haki', 
                    contenido: 'Poder del alma que ayuda a proteger la superficie de su piel, convitiendola en una superficie muy dura e impenetrable',
                    color: '#c56cf0'
                },{
                    'id': 3, 
                    titulo: 'Resistencia', 
                    contenido: 'Por su cuerpo hecho de goma puede resistir golpes, sana de manera rápida, absorbe mejor los golpes',
                    color: '#3ae374'
                }]
            }
        },
        components: {
            VCardMain
        }
    }
</script>

<style lang="scss" scoped>
    @import '../app';
    .skills {
        background-color: $color1;
        padding: 4em;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        &__title {
            font-family: $ff-primary;
            color: $color-white;
            margin-bottom: 1em;
            font-size: 24px;
        }
        &__text {
            font-family: $ff-secondary;
            color: $color-white;
            margin-bottom: 1em;
        }
        &__items {
            display: grid;
            grid-template-columns: 400px 400px;
        }
    }
</style>