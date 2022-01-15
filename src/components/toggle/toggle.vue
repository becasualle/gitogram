<template>
  <button :class="[{ active: show }, 'button']" @click="onToggle">
    <div>
      <span> {{ buttonText }} </span>
      <span class="icon">
        <!-- <icon icon-name="triangle"  /> -->
      </span>
    </div>
  </button>
</template>

<script>
// import {icon} from "@components/icon";
export default {
  // components {
  //     icon,
  // }
  emits: ['onToggle'],
  data() {
    return {
      show: false,
    };
  },
  computed: {
    buttonText() {
      return this.show ? 'Hide' : 'Show';
    },
  },
  methods: {
    onToggle() {
      this.show = !this.show;
      this.$emit('onToggle', this.show);
    },
  },
};
</script>

<style lang="scss" scoped>
.button {
  display: flex;
  align-items: center;
  padding: 0;
}
.icon {
  width: 10px;
  transform: rotate(180deg);
  transition: 0.4s;
}

.active {
  .icon {
    transform: rotate(0deg);
  }
}
</style>
