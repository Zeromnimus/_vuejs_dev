<template>
  <div>
    <h2>{{title}}</h2>
    <select>
      <option
        v-for="s in socialsList"
        :selected="s == defaultSocials"
      >{{ s }}</option>
    </select>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        title: 'Селекты VUE JS',
        socialsList: ['instagram', 'vk','facebook'],
        defaultSocials: 'vk',
      }
    },
  }

</script>

<style scoped>

</style>
