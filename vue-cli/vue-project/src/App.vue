<template>
  <div>
    <h2>{{title}}</h2>
    <textarea v-model="textarea"></textarea>
    <p>{{textarea}}</p>
  </div>

</template>

<script>
  export default {
    data() {
      return {
        title: 'Текстарея VUE JS',
        textarea: 'Initial textarea'
      }
    },
  }

</script>

<style scoped>
  textarea {
    height: 100px;
    width: 400px;
  }
  p {
    white-space: pre;
  }
</style>
