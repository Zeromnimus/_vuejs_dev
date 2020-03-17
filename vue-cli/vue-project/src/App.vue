<template>
  <div>
    <h2>{{title}}</h2>
    <input type="text" v-model.number="age">
    <p>{{age}}</p>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        title: 'Числовой модификатор VUE JS',
        age: 20
      }
    },
    watch: {
      age (value) {
        console.log(value)
        console.log(typeof value)
      }
    }
  }

</script>

<style scoped>

</style>
