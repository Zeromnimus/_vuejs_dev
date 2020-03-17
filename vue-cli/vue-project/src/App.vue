<template>
  <div>
    <h2>{{title}}</h2>
    <label>
      <input type="radio" value="instagram" v-model="social"> Instagram
    </label>
    <label>
      <input type="radio" value="vk" v-model="social"> Vk
    </label>
    <label>
      <input type="radio" value="ok" v-model="social"> OK
    </label>

    <hr>

    <p>
     {{social}}
    </p>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        title: 'Радио кнопки VUE JS',
        social: 'vk',
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
