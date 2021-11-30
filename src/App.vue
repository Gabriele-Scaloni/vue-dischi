<template>
  <div id="app">

  <GenereOption  @cambiagenere="filtragenere"/>

  <Principale :genereSelezionato="selezionato" />

  </div>
</template>

<script>

import Principale from '@/components/Principale.vue'

import GenereOption from '@/components/GenereOption.vue'


export default {
  name: 'App',
  components: {
    GenereOption,
    Principale,
  },
  data() {
    return {
      selezionato: "All"
    };
  },
  methods: {
  filtragenere(genere) {
        this.selezionato = genere;
      }
  }
}
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
