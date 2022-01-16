<template >
    <div class=user>
        <div class="user__avatar">
            <img :src="avatar" alt="username avatar" class="user__avatar__img" />
        </div>
        <div class="user__name ml-16">
            <p>{{ username }}</p>
        </div>
    </div>
</template>
<script>
export default {
    name: 'user',
    props: {
        avatar: {
            type: String,
            required: true,
        },
        username: {
            type: String,
            required: true,
        },
    }
    
}
</script>
<style lang="scss" src="./user.scss" scoped/>