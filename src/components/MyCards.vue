<template>
<div class="container-cards">
    <div class="cards">
        <img :src="details.poster" alt="album">
        <h3>{{details.title}}</h3>
        <span>{{details.author}}</span>
        <span>{{details.year}}</span>
    </div>
</div>
</template>

<script>
export default {
  name: 'MyMain',
  props: {
    details: Object,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
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
  background-color: #2e3a46;
  margin: 20px 10px;
}
img {
  width: 100px;
  height: 100px;
  object-fit: cover;
}
h3 {
  margin: 10px auto;
  color: white;
  text-align: center;
}
span {
  color: #808080;
  text-align: center;
}
</style>