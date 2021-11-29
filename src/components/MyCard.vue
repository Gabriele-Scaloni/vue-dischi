<template>

    <div class="cards">
        <img :src="details.poster" alt="album">
        <h3>{{details.title}}</h3>
        <span>{{details.author}}</span>
        <span>{{details.year}}</span>
    </div>

</template>

<script>
export default {
  name: 'MyCard',
  props: {
    details: Object,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.cards {
  width: 150px;
  height: 300px;
  padding: 15px;
  background-color: #2e3a46;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin: 20px 10px;
}
img {
  width: 120px;
  height: 120px;
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