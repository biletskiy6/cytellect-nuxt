<template>
  <div class="projects__item project">
    <div class="project__meta">
      <img
        src="https://pbs.twimg.com/profile_images/1002416157280727040/7SjA9KTJ_400x400.jpg"
        alt=""
        class="project__image"
      />

      <svg-icon v-if="warningIcon" name="warning" />
      <svg-icon v-if="checkIcon" name="check" />
      <svg-icon v-if="questionIcon" name="warning" />
    </div>
    <div class="project__about">
      <h3 class="project__header">Проект по заселению Марса</h3>

      <p v-if="fullText" class="project__text">
        Lorem Ipsum is simply dummy text of the printing and typesetting
        industry. Lorem Ipsum has been the industry's standard dummy text ever
        since the 1500s, when an unknown printer took a galley of type and
        scrambled it to make a type specimen book. It has survived not only five
        centuries, but also the leap into electronic typesetting, remaining
        essentially unchanged. It was popularised in the 1960s with the release
        of Letraset sheets containing Lorem Ipsum passages, and more recently
        with desktop publishing software like Aldus PageMaker including versions
        of Lorem Ipsum.
      </p>

      <p v-if="fullText" class="project__text">
        Lorem Ipsum is simply dummy text of the printing and typesetting
        industry. Lorem Ipsum has been the industry's standard dummy text ever
        since the 1500s, when an unknown printer took a galley of type and
        scrambled it to make a type specimen book. It has survived not only five
        centuries, but also the leap into electronic typesetting, remaining
        essentially unchanged. It was popularised in the 1960s with the release
        of Letraset sheets containing Lorem Ipsum passages, and more recently
        with desktop publishing software like Aldus PageMaker including versions
        of Lorem Ipsum.
      </p>

      <p v-if="!fullText" class="project__text">
        Краткое описание проекта по заселению марса нашими самыми лучшими
        колонистами - хомячками. Хомячки, это не только лучшие умы, но и лучшие
        хвосты, уши и лапы. Свободу действий хомякам!
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
            <li v-for="item in 3" :key="item" class="participants__item">
              <img
                src="https://pbs.twimg.com/profile_images/1002416157280727040/7SjA9KTJ_400x400.jpg"
                alt=""
                class="participants__image"
              />
            </li>
          </ul>
          <button class="project__button">
            <svg-icon name="plus-icon" />
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    warningIcon: {
      required: false,
      type: Boolean
    },
    checkIcon: {
      required: false,
      type: Boolean
    },
    questionIcon: {
      required: false,
      type: Boolean
    },
    fullText: {
      required: false,
      type: Boolean
    }
  },
  methods: {
    truncate(source, size) {
      return source.length > size ? source.slice(0, size - 1) + '…' : source
    }
  }
}
</script>
