<template>

<div class="container"> 
  <div class="container-cards">
    <!-- al posto di albums mettere generefiltrato-->
    <MyCard v-for="album in generefiltrato" 
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
/* import GenereOption from '@/components/GenereOption.vue' */


export default {
  name: 'Principale',
  components: {
    MyCard,
  },
  props :{
    genereSelezionato: String,
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
    methods: {
      getMyCard(){
        axios.get(this.apiUrl).then((result) => {
          this.albums = result.data.response;
        })
      },
    
    },
    computed: {
      generefiltrato(){
        let tutti = this.albums;
        let filtro = this.genereSelezionato;
        if (filtro === "All" ) {
          return tutti;
        } 

        tutti =  tutti.filter((elem) => {
          return elem.genre == filtro;
        })
        return tutti;
      }
    }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

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