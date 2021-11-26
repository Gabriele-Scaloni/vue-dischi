<template>
  <div id="app">
    
    <Principale/>

  </div>
</template>

<script>

import Principale from '@/components/Principale.vue'

export default {
  name: 'App',
  components: {
    Principale,
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
