<template>
  <div>
    <h2>{{title}}</h2>
    <app-ononff v-model="switched"></app-ononff>
    <div>
      <h3 v-if="switched">Component is enabled</h3>
      <h3 v-else="switched">Component is disbled</h3>
    </div>
  </div>
</template>

<script>
  import Onoff from './Onoff.vue'
  export default {
    data() {
      return {
        title: 'Создание своего контрола VUE JS',
        switched: true
      }
    },
    components: {
      appOnonff: Onoff
    }
  }

</script>

<style scoped>

</style>
