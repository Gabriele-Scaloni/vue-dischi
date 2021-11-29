<template>

    <div class="container-selezione">
        <span id="scelta"> Scegli il tuo genere  </span>
        <select @change="$emit('cambiagenere', selezionato)"
            v-model="selezionato">
            <option :value="all">all</option>
            <option :value="rock">rock</option>
            <option :value="pop">pop</option>
            <option :value="jazz">jazz</option>
            <option :value="metal">metal</option>
        </select>
    </div>
</template>

<script>
export default {
  name: 'GenereOption',
  data () {
      return {
        selezionato :Array,
      }

    }, 
   
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container-selezione {
    display: flex;
    align-items: center;
}
#scelta {
    color: white;
    margin-right: 10px;
}
</style>

