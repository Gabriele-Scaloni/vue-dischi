<template>

    <div class="container-selezione">
        <span id="scelta"> Scegli il tuo genere  </span>
        <select @change="$emit('cambiagenere', selezionato)">
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

/* <select v-model="selected">

  <option v-for="genere in genre" v-bind:value="option.value">
    {{ option.text }}
  </option>
</select>
<span>Selected: {{ selected }}</span>
new Vue({
  el: '...',
  data: {
    selected: 'A',
    genre: [
      { "tipo": "rock" },
      {  "tipo": "pop" },
      { "tipo": "jazz" }
    ]
  }
})  */
</style>

