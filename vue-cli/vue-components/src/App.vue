<template>
  <div class="container">
    <h1>{{title}}</h1>
    <ThumbSlider
    ></ThumbSlider>
    <hr>
    <input type="text" v-model="parentValue" @keypress.enter="setValue">
  </div>
</template>

<script>
import ThumbSlider from "./ThumbSlider";
import {EventEmitter} from './main.js'
export default {
    data () {
      return {
        title: "Тестирование компонента ползунок!",
        parentValue: 0
      }
    },
    methods: {
      setValue() {
        EventEmitter.$emit('onSetValue', this.parentValue )
        console.log(this.parentValue)
      }
    },
    components: {
      ThumbSlider: ThumbSlider
    },
  }
</script>
