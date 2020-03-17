<template>

  <div class="container">
    <h1>{{title}}</h1>
    <form class="pt-3">
    <div class="form-group">
      <label for="email">Email</label>
      <input
        type="email"
        id="email"
        class="form-control"
        @blur="$v.email.$touch()"
        v-model="email"
      >
    </div>
    </form>
    <pre>
      {{ $v.email }}
    </pre>
  </div>
</template>

<script>
  import { required, email } from 'vuelidate/lib/validators'
export default {
  data () {
      return {
        email: '',
        title: " Настройка валидаторов VUE JS"
      }
    },
      validations: {
        email: {
          required: required,
          email:email
        }
    }
  }

</script>
