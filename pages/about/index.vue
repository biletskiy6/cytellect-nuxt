<template>
  <div class="about-page">
    <AboutHero />
    <GrowBusiness />
  </div>
</template>

<script>
import AboutHero from '@/components/about-page/AboutHero'
import GrowBusiness from '@/components/about-page/GrowBusiness'
export default {
  name: 'Index',
  components: { GrowBusiness, AboutHero }
}
</script>

<style scoped></style>
