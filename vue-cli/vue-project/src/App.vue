<template>
  <div>
    <h2 v-colored:background.font = "'pink'">{{title}}</h2>
    <h2 v-colored:color.delay.font = "'blue'">{{title}}</h2>
    <hr>
    <h2 v-font>Local Font Directive</h2>
  </div>

</template>

<script>
export default {
    data() {
      return {
        title: 'Hello i am vue',

      }
    },
    directives: {
      font: {
        bind(el, bindings, vnode) {
          el.style.fontSize = '65px'
        }
      }
    }

  }

</script>
