<template>
  <div class="single-container">
    <div class="container">
      <h2 class="single-title">Mars terraforming project</h2>
      <div class="single-wrapper">
        <div class="single-left">
          <div class="single-left-container">
            <div class="project-container">
              <AppCard full-text />
            </div>
            <div class="project-more">
              <ul class="project-meta">
                <li class="project-meta__item">
                  <h3 class="project-meta__title">Assigned to: John Wick</h3>
                  <img
                    src="https://pbs.twimg.com/profile_images/1002416157280727040/7SjA9KTJ_400x400.jpg"
                    alt=""
                    class="project-meta__image"
                  />
                </li>
                <li class="project-meta__item">
                  <h3 class="project-meta__title">
                    Created by: Indiana Jounce
                  </h3>
                  <img
                    src="https://pbs.twimg.com/profile_images/1002416157280727040/7SjA9KTJ_400x400.jpg"
                    alt=""
                    class="project-meta__image"
                  />
                </li>
                <li class="project-meta__item">
                  <h3 class="project-meta__title">
                    Last edit: Jony Mnemony
                  </h3>
                  <img
                    src="https://pbs.twimg.com/profile_images/1002416157280727040/7SjA9KTJ_400x400.jpg"
                    alt=""
                    class="project-meta__image"
                  />
                </li>
              </ul>

              <div class="voting-container">
                <h3 class="voting-title">Voting</h3>
                <ul class="voting">
                  <li class="voting__item">
                    <span class="voting__text">Accent</span>
                    <span class="warning">10</span>
                  </li>
                  <li class="voting__item">
                    <span class="voting__text">Reject</span>
                    <span class="danger">2</span>
                  </li>
                </ul>
              </div>
            </div>
          </div>
          <div class="single-comments">
            <LeaveAComment />
            <div class="project-comments">
              <ProjectComment v-for="item in 2" :key="item" />
            </div>
          </div>
        </div>
        <div class="single-right">
          <AppCard v-for="item in 5" :key="item" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import LeaveAComment from '@/components/LeaveAComment'
import ProjectComment from '@/components/ProjectComment'
export default {
  name: 'Index',
  layout: 'auth',
  components: { ProjectComment, LeaveAComment }
}
</script>
