<template>

<div class="container">
  <div id="navbar"> <img id="logonav" src="https://www.logolynx.com/images/logolynx/51/51b63b09d988d4545d7e6db63cdb8cd8.png" alt="Logo spotify">
    <GenereOption @filtragenere="cambiagenere"/>
  </div>
  <div class="container-cards">
    <!-- al posto di albums mettere filtragenere -->
    <MyCard v-for="album in albums" 
    :key="album.id"
    :details="album" 
    />
  </div>
</div>
</template>

<script>
//importo axios e lo installo del terminale, prima uscendo dal progetto
import axios from 'axios';
//importo qui MyCards (component figlio di questo componente)
import MyCard from '@/components/MyCard.vue'
import GenereOption from '@/components/GenereOption.vue'


export default {
  name: 'Principale',
  components: {
    MyCard,
    GenereOption
  },
  data() {
    return {//inserire in apiUrl l'url dell'array
      apiUrl :"https://flynn.boolean.careers/exercises/api/array/music",
      albums: [],
    }
  },
  created() {
    this.getMyCard();
  },
    methods :{
      getMyCard(){
       axios
      .get(this.apiUrl)
      .then((result) => {
        this.albums = result.data.response;
      }
      )}
    },
    computed: {
        filtragenere(){
       return
    }
    }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#navbar {
  width:100%;
  height: 60px;
  background-color:#2e3a46;
  display: flex;
}
#navbar:after {
  content: "";
  display: table;
  clear: both;
}
#logonav {
  width: 40px;
  height: 40px;
  float: left;
  margin: 10px;
}
.container {
  background-color: #1e2d3b;
  width:100%;
  height: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
}
.container-cards {
  width: 90%;
  height: auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin: 20px auto;
}
</style>