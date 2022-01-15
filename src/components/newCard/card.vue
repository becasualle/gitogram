<template>
  <div class="card">
    <div class="card__title_wrap mb-16">
      <h2 class="card__title">Title</h2>
    </div>
    <div class="card__desc mb-32">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Iure repellat
      labore nam dicta nulla. Voluptate sequi possimus quia corporis ea minus.
      Sunt, temporibus officiis accusamus eum dicta ducimus dolor quaerat?
    </div>
    <div class="card__stats">
      <!-- <stats :stars="10" :forks="5"> -->
    </div>
  </div>
</template>

<script>
// import {stats} from "@components/stats"
export default {
  // components {
  //     stats,
  // }
  // props: {
  //   title:
  // }
};
</script>

<style lang="scss" scoped>
.card {
  background: #ffffff;
  border: 1px solid #f1f1f1;
  box-shadow: 0px 4px 40px rgba(0, 0, 0, 0.07);
  border-radius: 10px;
  padding: 24px 20px;
}
</style>
