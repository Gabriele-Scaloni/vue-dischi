<template>
    <div id="navbar"> 
        <img id="logonav" src="https://www.logolynx.com/images/logolynx/51/51b63b09d988d4545d7e6db63cdb8cd8.png" alt="Logo spotify">  
    <!-- con emit invio cose dal "figlio" al "genitore", con le props 
    il contrario -->
    <span>Seleziona il genere</span>
        <select id="selectgenere" @change="$emit('cambiagenere', selezionato)"
            v-model="selezionato">
            <option value="All">All</option>
            <option value="Rock">rock</option>
            <option value="Pop">pop</option>
            <option value="Jazz">jazz</option>
            <option value="Metal">metal</option>
        </select>
    </div>
</template>

<script>
export default {
  name: 'GenereOption',
  
  data () {
      return {
        selezionato: "All",
      }
    }, 
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
#selectgenere {
    margin: 15px 5px;
    height: 30px;
}
#logonav {
  width: 40px;
  height: 40px;
  float: left;
  margin: 10px;
}
span {
    align-self: center;
    color: white;
}
</style>

