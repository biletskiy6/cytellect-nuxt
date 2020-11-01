<template>
  <div class="app-navigation">
    <ul class="menu">
      <li class="menu__item">
        <nuxt-link class="menu__link" to="/about">About</nuxt-link>
      </li>
      <li class="menu__item">
        <nuxt-link class="menu__link" to="/">Products</nuxt-link>
      </li>
      <li class="menu__item">
        <nuxt-link class="menu__link" to="/">Contact</nuxt-link>
      </li>
      <li class="menu__item">
        <nuxt-link class="menu__link" to="/">Help</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'AppNavigation'
}
</script>
