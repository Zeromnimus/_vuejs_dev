<template>
    <div class="slidecontainer">
      <input type="range"
             :min="minVal"
             :max="maxVal"
             class="slider"
             id="myRange"
             v-model="value"
      >
      <p>Value: <span id="demo">{{value}}</span></p>
    </div>
</template>

<script>
  import {EventEmitter} from "./main";

  export default {
      name: "ThumbSlider",
      data () {
        return {
          minVal: 1,
          maxVal: 100,
          value: 50,
        }
      },
      created() {
        EventEmitter.$on('onSetValue', (nval) => {
          this.value = nval
        })
      }
    }
</script>

<style scoped>
  .slidecontainer {
    width: 100%;
  }

  .slider {
    -webkit-appearance: none;
    width: 100%;
    height: 10px;
    border-radius: 5px;

    background: url('./assets/line.png');
    outline: none;
    opacity: 0.7;
    -webkit-transition: .2s;
    transition: opacity .2s;
    border: 1px solid black;
  }

  .slider:hover {
    opacity: 1;
  }

  .slider::-webkit-slider-thumb {
    -webkit-appearance: none;
    appearance: none;
    width: 23px;
    height: 24px;
    border: 0;
    background: url('./assets/pipka.png');
    cursor: pointer;
  }

  .slider::-moz-range-thumb {
    width: 23px;
    height: 24px;
    border: 0;
    background: url('./assets/pipka.png');
    cursor: pointer;
  }
</style>
