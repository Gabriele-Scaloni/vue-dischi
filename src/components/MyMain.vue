<template>

<div class="container">

  <div id="navbar"> </div>
 
  <div class="container-cards">
    <div class="cards">
    <img src="" alt="album">
    <h3>album323</h3>
    <span>23</span>
  </div>
  </div>
  
</div>
</template>

<script>
export default {
  name: 'MyMain',
  props: {

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#navbar {
  width:100vw;
  height: 5vh;
  background-color:#2e3a46 ;
}
.container {
  background-color: #1e2d3b;
  width:100vw;
  height: 95vh;
}
.container-cards {
  width: 80%;
  height: auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
  
  margin: 20px auto;
}
.cards {
  width: 150px;
  height: 250px;
  padding: 5px;
}
img {
  width: 100px;
  height: 100px;
  object-fit: cover;
  background-color: #2e3a46;
}
h3 {
  color: white;
  text-align: center;
}
span {
  color: #808080;
  text-align: center;
}
</style>