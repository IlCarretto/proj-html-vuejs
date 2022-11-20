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
        <div class="top-content">
            <p>{{subtitle}}</p>
        </div>
        <div class="bottom-content">
            <img :src="getImgUrl(imgSrc)" alt="">
            <h3 class="">{{title}}</h3>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables.scss" as *;

    p {
        color: $grey-text;
    }

    h3 {
        color: $gold-text;
        font-size: 1rem;
        margin-top: 1rem;
    }

    img {
        width: 100px;
        height: 100px;
        border-radius: 50%;
    }
</style>