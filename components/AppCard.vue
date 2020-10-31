<template>
  <div class="projects__item project">
    <div class="project__meta">
      <img
        src="https://pbs.twimg.com/profile_images/1002416157280727040/7SjA9KTJ_400x400.jpg"
        alt=""
        class="project__image"
      />
    </div>
    <div class="project__about">
      <h3 class="project__header">Проект по заселению Марса</h3>
      <p class="project__text">
        {{ truncate('Lorem Ipsum Odr', 4) }}
      </p>

      <div class="project__bottom">
        <div class="project__author author">
          <img
            class="author__image"
            src="https://pbs.twimg.com/profile_images/1002416157280727040/7SjA9KTJ_400x400.jpg"
            alt=""
          />
          <div class="author__about">
            <h4 class="author__name">John Doe</h4>
            <span class="circle"></span>
            <div class="author__stamp">5 minutes ago</div>
          </div>
        </div>
        <div class="project__participants">
          <ul class="participants">
            <li class="participants__item">
              <img
                src="https://pbs.twimg.com/profile_images/1002416157280727040/7SjA9KTJ_400x400.jpg"
                alt=""
                class="participants__image"
              />
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  methods: {
    truncate(source, size) {
      return source.length > size ? source.slice(0, size - 1) + '…' : source
    }
  }
}
</script>
