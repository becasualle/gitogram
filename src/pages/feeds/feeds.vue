<template>
  <div class="topline">
    <!-- Шапка с навигацией и контентом -->
    <topline>
      <template #headline>
        <div class="navbar">
          <logo />
          <div class="navbar__icons">
            <icon iconName="home" class="icon"/>
            <icon iconName="signOut" class="icon"/>
          </div>
        </div>
      </template>
      <template #content>
        <ul class="stories">
          <li v-for="story in stories" :key="story.id" class="stories-item">
            <story-user-item
              :avatar="story.avatar"
              :username="story.username"
            />
          </li>
        </ul>
        <feed />
      </template>
    </topline>
  <!-- страница постов -->
    <div class="posts-container">
    <ul class="posts__list">
      <li v-for="post in posts" :key="post.id" class="posts__item">
        <post :avatar="post.avatar" :username="post.username">
          <template #card> <card /> </template>
        </post>
      </li>
    </ul>
  </div>
  </div>
</template>

<script>
import { topline } from "../../components/topline";
import { storyUserItem } from "../../components/storyUserItem";
import { logo } from "../../components/logo";
import { icon } from "../../icons";
import { feed } from "../../components/feed";
import { post } from "../../components/post";
import { card } from "../../components/card";
import stories from "./data.json";
import posts from "./posts.json";

export default {
  name: "Feeds",
  components: {
    topline,
    icon,
    storyUserItem,
    logo,
    feed,
    post,
    card,
  },
  data() {
    return {
      stories: [],
      posts: [],
    };
  },
  created(){
    this.posts = posts;
    this.stories = stories;
  }
};
</script>

<style lang="scss" src="./feeds.scss" scoped />
