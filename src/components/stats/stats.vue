<template>
    <div class="stats">
        <div class="stats__stars">
            <div class="stats__stars__title">
                <icon iconName="star" class="icon mr-12 ml-4"/>
          
                <p>Star</p>
            </div>
            <div class="stats__stars__value">
                <p>{{stars}}</p>
            </div>
        </div>

        <div class="stats__forks">
            <div class="stats__forks__title">
                <icon iconName="fork" class="icon mr-12 ml-4"/>
                <p>Fork</p>
            </div>
            <div class="stats__forks__value">
                <p>{{forks}}</p>
            </div>
        </div>

    </div>
</template>

<script>
 import { icon } from "../../icons";
export default {
   
    name: 'stats',
    components: {
        icon,
    },
    props: {
        stars: {
            type: Number,
            default: 10,
            required: true,
        },
        forks: {
            type: Number,
            default: 5,
            required: true,
        },
    }
}
</script>

<style lang="scss" scoped src="./stats.scss">

</style>