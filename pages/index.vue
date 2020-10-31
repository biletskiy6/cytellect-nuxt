<template>
  <div class="home">
    <div class="title">All</div>
    <div class="projects">
      <AppCard :key="item" v-for="item in 5" />
    </div>
  </div>
</template>
