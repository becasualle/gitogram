<template>
  <component :is="iconName" />
</template>

<script>
import * as icons from './variants';
export default {
  name: "Icon",
  components: { ...icons },
  props: {
    iconName: {
      type: String,
      required: true,
      validator(value) {
        return Object.keys(icons).includes(value);
      },
    },
  },
};
</script>
