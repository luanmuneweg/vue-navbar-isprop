<template>
  <div class="navegacao">
    <button v-for="(_, comp) in comps" :key="comp" :class="['botao', {active: compExibido === comp}]" @click="compExibido = comp">
      {{comp}}
    </button>

    <component :is="comps[compExibido]"></component>
  </div>
</template>

<script setup>
import Home from './shared/Home.vue'
import Projetos from './shared/Projetos.vue'
import Serviços from './shared/Servicos.vue'
import Contato from './shared/Contato.vue'
import { ref } from 'vue'

const compExibido = ref('Home')

const comps = {
  Home,
  Projetos,
  Serviços,
  Contato
}
</script>

<style scoped>
.botao {
  padding: 10px 30px;
  font-size: 20px;
  color: rgb(77, 59, 0);
}
.botao.active {
  background-color: rgba(203, 204, 170, 0.986);
}
</style>
