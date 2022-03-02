<template>
<navegacao></navegacao>
</template>

<script>
import navegacao from './components/navegacao.vue'

export default {
  name: 'App',
  components: {
    navegacao: navegacao
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
