<template>

    <div class="container-selezione">
        <span id="scelta"> Scegli il tuo genere  </span>
        <select v-model="selected">
            <option>All</option>
            <option>Rock</option>
            <option>Pop</option>
            <option>Jazz</option>
            <option>Metal</option>
        </select>
    </div>
</template>

<script>
export default {
  name: 'GenereOption',
  props: {
  }
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