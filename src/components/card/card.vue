<template>
  <div class="card">
    <div class="card__title_wrap mb-16">
      <h2 class="card__title">Vue.js</h2>
    </div>
    <div class="card__desc mb-32">
      JavaScript framework for building interactive web applications ⚡
    </div>
    <div class="card__stats">
      <stats :stars="10" :forks="5"/>
    </div>
  </div>
</template>

<script>
import { stats } from "../stats";
export default {
  components: {
      stats,
  }
};
</script>

<style lang="scss" scoped src="./card.scss">

</style>
