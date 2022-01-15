<template>
  <div class="post">
    My post component
    <div class="post__user mb-16">
      <!-- <user :src="avatar_url" :name="username"/> -->
    </div>
    <div class="post__card mb-16">
      <slot name="card" />
    </div>
    <toggle @onToggle="toggleClick" />
    <div v-if="showComment">
      <ul class="post__comment comment__list">
        <li v-for="item in 5" :key="item" class="comment__item">
          <p>
            <span class="comment__user"> User name </span>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit.
            Necessitatibus recusandae dolore facere quas consequuntur repellat
            fuga ratione quia, quidem sapiente est cupiditate. Culpa, sequi?
            Veniam quia aliquid ducimus repellat voluptatem!
          </p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import { toggle } from '../toggle';
// import {user} from "@components/user"
export default {
  components: {
    toggle,
  },
  props: {
    avatar_url: {
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

<style lang="scss" scoped></style>
