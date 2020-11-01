<template>
  <div class="auth-layout">
    <AppAuthHeader />
    <nuxt />
  </div>
</template>

<script>
export default {
  head() {
    return {
      bodyAttrs: {
        class: 'auth'
      }
    }
  }
}
</script>
