<template>
    <div class="is-flex is-align-items-center is-justify-content-space-beteen">
        <Cronometro :tempoEmSegundos="tempoEmSegundos" />
        <button class="button" @click="iniciar" :disabled="cronometroRodando">
            <span class="icon">
                <i class="fas fa-play"></i>
            </span>
        </button>
        <button class="button" @click="pausar" :disabled="!cronometroRodando">
            <span class="icon">
                <i class="fas fa-pause"></i>
            </span>
        </button>
        <button class="button" @click="finalizar" :disabled="!cronometroRodando">
            <span class="icon">
                <i class="fas fa-stop"></i>
            </span>
        </button>
    </div>
</template>

<script lang="ts">
    import {defineComponent} from 'vue';
    import Cronometro from './Cronometro.vue';

    export default defineComponent({
        name: 'Temporizador',
        emits: ['aoTemporizadorFinalizado'],
        components: {
            Cronometro
        },
        data(){
            return{
                tempoEmSegundos: 0,
                cronometro: 0,
                cronometroRodando: false
            }
        },        
        methods: {
            iniciar(){
                this.cronometroRodando = true;
                this.cronometro = setInterval(()=>{
                    this.tempoEmSegundos += 1
                }, 1000)
            },
            pausar(){
                this.cronometroRodando = false;
                clearInterval(this.cronometro);
            },
            finalizar(){
                this.cronometroRodando = false;
                this.$emit('aoTemporizadorFinalizado', this.tempoEmSegundos);
                clearInterval(this.cronometro);
                this.tempoEmSegundos = 0;
            }
        }
    });
</script>