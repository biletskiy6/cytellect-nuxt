<template>
  <div class="signup">
    <div class="signup-container">
      <form class="auth-form" action="#" @submit.prevent="handleSubmit">
        <div class="auth-form__field">
          <label for="login" class="auth-form__label">Login</label>
          <input
            id="login"
            v-model="login"
            name="login"
            type="text"
            class="auth-form__input"
          />
          <span class="border"></span>
          <p v-if="$v.login.$dirty && $v.login.$error" class="error-message">
            Field is required
          </p>
        </div>

        <div class="auth-form__field">
          <label for="login" class="auth-form__label">Password</label>
          <input
            id="password"
            v-model="password"
            name="password"
            type="password"
            class="auth-form__input"
          />
          <span class="border"></span>
          <p
            v-if="$v.password.$dirty && $v.password.$error"
            class="error-message"
          >
            Minimal length for the password is
            {{ $v.password.$params.minLength.min }} symbols
          </p>
        </div>
        <div class="auth-form__confirm">
          <button class="button" type="submit">Login</button>
          <button class="button" @click="handleCancelClick">Cancel</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
import { required, minLength } from 'vuelidate/lib/validators'
export default {
  name: 'Index',
  data() {
    return {
      login: '',
      password: ''
    }
  },
  methods: {
    handleCancelClick() {
      this.$router.push({ name: 'index' })
    },
    handleSubmit() {
      if (this.$v.$invalid) {
        this.$v.$touch()
        return
      }
      this.$router.push({ name: 'account' })
    }
  },
  validations: {
    login: {
      required
    },
    password: {
      required,
      minLength: minLength(8)
    }
  }
}
</script>
