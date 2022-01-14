<template>
  <about />
  <feeds />
</template>

<script>
import {about} from "./components/about";
import {feeds} from "./pages/feeds";

export default {
  name: "App",
  components: {
    about,
    feeds,
  },
};
</script>

<style lang='scss' src='./global.scss'>

</style>
