<template>
  <div>
    <h2>{{title}}</h2>
    <input type="text" v-model.lazy="name">
    <p>{{name}}</p>
  </div>

</template>

<script>
  export default {
    data() {
      return {
        title: 'Текстовый инпут VUE JS',
        name: 'Initial state'
      }
    },
  }

</script>
