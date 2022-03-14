<template>
  <div class="navegacao">
    <button :value="comp" v-for="(_,comp) in comps" :key="comp.id" :class="['botao', {active: compExibido === comp}]" @click="$emit('update:compExibido', $event.target.value)">
      {{comp}}
    </button>
  </div>
</template>

<script>
  export default {
    props:{
      comps: Object,
      compExibido: String
    },

    emits:
      ['update:compExibido']
      
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
