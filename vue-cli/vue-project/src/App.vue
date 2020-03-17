<template>
  <div>
    <h2>{{title}}</h2>
    <select v-model="socials">
      <option
        v-for="s in socialsList"
        :selected="s == defaultSocials"
      >{{ s }}</option>
    </select>
    <hr>
    <p>{{ socials }}</p>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        title: 'Селекты VUE JS',
        socialsList: ['instagram', 'vk','facebook'],
        defaultSocials: 'vk',
        socials: 'vk'
      }
    },
  }

</script>

<style scoped>

</style>
