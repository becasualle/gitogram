<template>
  <div class="topline">
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
  </div>
</template>

<script>
import { topline } from "../../components/topline";
import { storyUserItem } from "../../components/storyUserItem";
import { logo } from "../../components/logo";
import { icon } from "../../icons";
import stories from "./data.json";
import { feed } from "../../components/feed";

export default {
  name: "Feeds",
  components: {
    topline,
    icon,
    storyUserItem,
    logo,
    feed,
  },
  data() {
    return {
      stories,
    };
  },
};
</script>

<style lang="scss" src="./feeds.scss" scoped />
