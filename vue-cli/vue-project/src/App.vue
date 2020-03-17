<template>
  <div>
    <h2>{{title}}</h2>
    <input type="text" v-model="searchName">
    <ul>
      <li v-for="name in filteredNames"> {{ name }}</li>
    </ul>
  </div>

</template>

<script>
export default {
    data() {
      return {
        title: 'Фильтрация списков',
        searchName: '',
        names: ['Vlad', 'Max', 'Elena', 'Igor']
      }
    },
    computed: {
      filteredNames() {
        return this.names.filter(name => {
          return name.toLowerCase().indexOf(this.searchName.toLowerCase()) !== -1
        })
      }
    },
    filters: {
      lowercase(value) {
        return value.toLowerCase()
      }
    }
  }

</script>

<style scoped>

</style>
