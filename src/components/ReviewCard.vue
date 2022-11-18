<script>
import {store} from "../store";

export default {
    name: "ReviewCard",
    props: {
        subtitle: String,
        imgSrc: String,
        title: String,
    },
    data() {
        return {
            
        }
    },
    methods: {
        getImgUrl(imgName) {
                return new URL(`../assets/${imgName}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="ms-card">
        <div class="text-content">
            <h3 class="">{{title}}</h3>
            <p>{{subtitle}}</p>
        </div>
        <div class="img-content">
            <img :src="getImgUrl(imgSrc)" alt="">
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>