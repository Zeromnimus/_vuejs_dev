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
        :class="{'is-invalid': $v.email.$error}"
        @blur="$v.email.$touch()"
        v-model="email"
      >
      <div class="invalid-feedback" v-if="!$v.email.required">Email field is required.</div>
      <div class="invalid-feedback" v-if="!$v.email.email">This field should be an email.</div>
    </div>
    </form>
  </div>
</template>

<script>
  import { required, email } from 'vuelidate/lib/validators'
export default {
  data () {
      return {
        email: '',
        title: "Визуальное отображение ошибок VUE JS"
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
