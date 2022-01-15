<template>
    <button :class="['button', {'active':isOpened}]" @click="toggleActive">
        <span class="text"> {{ isOpened ? 'Hide' : 'True' }} issues </span>
        <span class="icon"> 
            <icon iconName="triangle" />
        </span>
    </button>
</template>

<script>
import { icon } from "../../icons";
export default {
    name: 'toggler',
    components: {
        icon,
    },
    data() {
        return {
            isOpened: false,
        }
    },
    methods: {
        toggleActive() {
            this.isOpened = !this.isOpened;
            this.$emit("onToggle", this.isOpened)
        }
    }
};
</script>

<style lang="scss" src="./toggler.scss" scoped>
</style>
