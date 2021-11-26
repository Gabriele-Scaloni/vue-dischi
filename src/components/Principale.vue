<template>

<div class="container">
  <div id="navbar"> </div>
 
  <MyCards/>
 
</div>
</template>

<script>
import MyCards from '@/components/MyCards.vue'


export default {
  name: 'Principale',
  components: {
    MyCards
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#navbar {
  width:100%;
  height: 50px;
  background-color:#2e3a46 ;
}
.container {
  background-color: #1e2d3b;
  width:100%;
  height: 100%;
}

</style>