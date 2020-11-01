<template>
  <div class="app-header">
    <div class="container">
      <div class="app-header-wrapper">
        <Logo />
        <AppNavigation />

        <div class="auth-buttons">
          <nuxt-link class="auth-link auth-link--login" to="/"
            >Sign In</nuxt-link
          >
          <nuxt-link class="auth-link auth-link--register button" to="/sign-up"
            >Sign Up</nuxt-link
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AppNavigation from '@/components/AppNavigation'
export default {
  name: 'AppHeader',
  components: { AppNavigation }
}
</script>
