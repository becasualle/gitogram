<template>
  <div class="post">
    <!-- аватар и имя пользователя -->
    <div class="post__user mb-16">
      <user :avatar="avatar" :username="username" />
    </div>
    <!-- слот под контент поста -->
    <div class="post__card mb-16">
      <slot name="card" />
    </div>
    <!--  -->
    <!-- тогглер комментариев -->
    <toggler @onToggle="toggleClick" />
    <div v-if="showComment">
      <ul class="post__comment comment__list mt-12 mb-12">
        <li v-for="item in 3" :key="item" class="comment__item">
          <p>
            <span class="comment__user"> Marselle </span>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. At, molestias.
          </p>
        </li>
      </ul>
    </div> 

  </div>
</template>

<script>
import { user } from "../user";
import {toggler} from "../toggler";

export default {
  components: {
    user,
    toggler
  },
  props: {
    avatar: {
      type: String,
      default: '',
    },
    username: {
      type: String,
      default: 'User Loft',
    },
  },
  data() {
    return {
      showComment: false,
    };
  },
  methods: {
    toggleClick(state) {
      this.showComment = state;
    },
  },
};
</script>

<style lang="scss" src="./post.scss" scoped>
</style>
