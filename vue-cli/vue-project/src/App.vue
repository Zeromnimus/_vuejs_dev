<template>
  <div>
    <h2>{{title}}</h2>
    <input type="text" v-model="searchName">
    <ul>
      <li v-for="name in filteredNames"> {{ name }}</li>
    </ul>
    <hr>
    <app-list></app-list>
  </div>

</template>

<script>
  import ListMixin from './listMixin'
export default {
    data() {
      return {
        title: 'Использование миксинов VUE JS',
      }
    },
  mixins: [ListMixin],
    filters: {
      lowercase(value) {
        return value.toLowerCase()
      }
    }
  }

</script>

<style scoped>

</style>
