<template>
  <div class="posts-container">
    Posts page
    <ul class="post__list">
      <li v-for="(item, index) in 5" :key="index" class="post__item">
        <post>
          <template #card> <card /> </template>
        </post>
      </li>
    </ul>
  </div>
</template>

<script>
import { post } from '../../components/post';
import { card } from '../../components/newCard';
// import {data} from

export default {
  components: {
    post,
    card,
  },
  data() {
    return {
      posts: [],
    };
  },
  // created() {
  //   console.log(data);
  //   this.posts = data;
  // },
};
</script>

<style lang="scss" scoped>
.posts {
  &-container {
    width: 979px;
    margin: 0 auto;
  }
  &__item {
    margin-bottom: 20px;
  }
}
</style>
