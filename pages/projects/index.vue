<template>
  <div class="dashboard">
    <div class="container">
      <div class="favorites">
        <div class="title">Favorites</div>
        <div class="projects">
          <AppCard
            v-for="(item, index) in 3"
            :key="item"
            :warning-icon="index === 0"
            @click.native="handleCardClick"
          />
        </div>
      </div>

      <div class="all">
        <div class="title">All</div>
        <div class="projects">
          <AppCard
            v-for="(item, index) in 6"
            :key="item"
            :warning-icon="index === 0"
            :check-icon="index === 1"
            :question-icon="index === 2"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'auth',
  methods: {
    handleCardClick() {
      this.$router.push({
        name: 'project-slug',
        params: { slug: 'mars-project' }
      })
    }
  }
}
</script>
