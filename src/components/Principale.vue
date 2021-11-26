<template>

<div class="container">
  <div id="navbar"> </div>
 
  <MyCards v-for="album in albums" 
   :key="album.id"
   :details="album" 
   />
 
</div>
</template>

<script>
//importo axios e lo installo del terminale, prima uscendo dal progetto
import axios from 'axios';
//importo qui MyCards (component figlio di questo componente)
import MyCards from '@/components/MyCards.vue'


export default {
  name: 'Principale',
  components: {
    MyCards
  },
  data() {
    return {//inserire in apiUrl l'url dell'array
      apiUrl :"https://flynn.boolean.careers/exercises/api/array/music",
      albums: [],
    }
  },
  created() {
    this.getMyCards();
  },
    methods :{
      getMyCards(){
       axios
      .get(this.apiUrl)
      .then((result) => {
        this.albums = result.data;
      }
      )}
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