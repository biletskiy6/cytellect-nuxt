<template>
  <div class="leave-comment">
    <img
      class="leave-comment__author"
      src="https://pbs.twimg.com/profile_images/1002416157280727040/7SjA9KTJ_400x400.jpg"
      alt=""
    />
    <input
      v-model="comment"
      class="leave-comment__input"
      type="text"
      placeholder="Leave a comment here"
    />
  </div>
</template>

<script>
export default {
  name: 'LeaveAComment',
  data() {
    return {
      comment: ''
    }
  }
}
</script>
