<template>
  <div class="default">
    <AppHeader />
    <nuxt />
  </div>
</template>

<script>
import AppHeader from '@/components/AppHeader'
export default {
  name: 'Default',
  components: { AppHeader }
}
</script>
