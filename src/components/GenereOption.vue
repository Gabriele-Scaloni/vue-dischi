<template>
    <div class="container-selezione">
        <span id="scelta"> Scegli il tuo genere  </span>
        <!-- con emit invio cose dal "figlio" al "genitore", con le props 
        il contrario -->
        <select @change="$emit('cambiagenere', selezionato)"
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

#scelta {
    color: white;
    margin-right: 10px;
}
</style>

