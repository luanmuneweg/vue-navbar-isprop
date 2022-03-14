<template>
  <div>
    <navegacao :comps="comps" v-model:compExibido="compExibido">
    </navegacao>
    <component :is="comps[compExibido]"></component>
  </div>
</template>

<script>
  import navegacao from './components/navegacao.vue'
  import Home from './components/shared/Home.vue'
  import Projetos from './components/shared/Projetos.vue'
  import Serviços from './components/shared/Servicos.vue'
  import Contato from './components/shared/Contato.vue'

  export default {
    name: 'App',
    
    components: {
      navegacao: navegacao
    },

    data() {
      return {
        comps: {
          Home,
          Projetos,
          Serviços,
          Contato
        }, 

        compExibido: 'Home'
      }
    }
  }

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
