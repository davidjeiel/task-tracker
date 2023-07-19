<template>
  <main class="columns is-gapless is-multiline modo-escuro">   
    <div class="column is-tree-quarter conteudo">
      <Formulario @aoSalvarTarefa="salvarTarefa"/>
      <div class="lista">
        <Tarefa v-for="(tarefa, index) in tarefas" :key="index" :tarefa="tarefa" />          
      </div>
    </div>
  </main>
</template>

<script lang="ts">
  import {defineComponent } from 'vue';
  import Formulario   from './components/Formulario.vue';
  import Tarefa   from './components/Tarefa.vue';
  import ITarefa from './interfaces/ITarefa';

  export default defineComponent({
      name: "App",
      components: { Formulario, Tarefa },
      data (){
        return{
          tarefas: [] as ITarefa[]
        }
      },
      methods: {
        salvarTarefa(tarefa: ITarefa){
          this.tarefas.push(tarefa);
        }
      }
  });
</script>

<style>
.lista{
  padding:1.25rem;
}
main{
  --bg-primario: #fff;
  --texto-primario: #000;
}
main.modo-escuro{
  --bg-primario: #2b2bd42;
  --texto-primario: #ddd;
}
.conteudo{
  background-color: var( --bg-primario );
}
</style>