<template>
  <div>
    <h2>{{title}}</h2>
    <label>
      <input type="checkbox" value="instagram" v-model="social"> Instagram
    </label>
    <label>
      <input type="checkbox" value="vk" v-model="social"> Vk
    </label>
    <label>
      <input type="checkbox" value="ok" v-model="social"> OK
    </label>

    <hr>

    <ul>
      <li v-for="s in social">{{s}}</li>
    </ul>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        title: 'Чекбоксы VUE JS',
        social: ['vk'],
        s: ''
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
