<template>
  <nuxt-link class="logo" to="/">
    <svg-icon name="logo" />
    <span class="logo__text">Cytellect</span>
  </nuxt-link>
</template>
<style>
.NuxtLogo {
  animation: 1s appear;
  margin: auto;
}

@keyframes appear {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
