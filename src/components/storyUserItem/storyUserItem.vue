<template>
  <button class="c-story-user-item" @click="$emit('onPress')">
    <div class="avatar">
      <img :src="avatar" alt="username avatar" class="img" />
    </div>
    <div class="username mt-16">{{ username }}</div>
  </button>
</template>
<script>
export default {
  name: "StoryUserItem",
  props: {
    avatar: {
      type: String,
      required: true,
    },
    username: {
      type: String,
      required: true,
    },
  },
};
</script>
<style lang="scss" src="./storyUserItem.scss" scoped></style>
