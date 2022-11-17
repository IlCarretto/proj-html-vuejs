<script>
export default {
    name: "AppCard",
    props: {
        imgSrc: String,
        title: String,
        subtitle: String
    },
    data() {
        return {
            
        }
    }
}
</script>

<template>
    <div class="ms-card">
        <div class="img-content">
            <img :src="imgSrc" alt="">
        </div>
        <div class="text-content">
            <h3 class="gold-title">{{title}}</h3>
            <p>{{subtitle}}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
</style>