<template>
  <div id="app">
    
    <MyMain/>

  </div>
</template>

<script>

import MyMain from '@/components/MyMain.vue'

export default {
  name: 'App',
  components: {
    MyMain,
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
