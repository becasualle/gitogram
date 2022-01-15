<template>
  <div class="c-topline">
    <div class="x-container">
      <div class="headline">
        <slot name="headline" />
      </div>
      <div v-if="$slots.content" class="content">
        <slot name="content" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Topline',
};
</script>

<style lang="scss" src="./topline.scss" scoped></style>
