<script>
import AppCard from './AppCard.vue';
import ReviewCard from "./ReviewCard.vue";

export default {
    name: "AppMain",
    components: {
        AppCard,
        ReviewCard
    }, 
    data() {
        return {
            services: [
                {
                    src: "avadabarbers-trimcut-icon-before.png",
                    title: "Trim & Cut",
                    subtitle: "Avada Barbers are experts in the lickety split trim and hair cut. Quick but careful and ridiulously good looking."
                },
                {
                    src: "avadabarbers-washndry-icon.png",
                    title: "Wash & Dry",
                    subtitle: "Take a seat in our fine leather chairs, lean back and let us lather you a fresh head in a luxurious fashion."
                },
                {
                    src: "avadabarbers-beardtrim-icon.png",
                    title: "Beard Tidy",
                    subtitle: "Tame the tangles and untidy facial hairs like a gentleman with our Beard Tidy services from Avada Barbers."
                },
            ],
            products: [
                {
                    src: "brush_dark.png",
                    title: "Brush",
                    subtitle: "$15.00"
                },
                {
                    src: "scissors.png",
                    title: "Scissors",
                    subtitle: "$85.00"
                },
                {
                    src: "hot_oil_dark.png",
                    title: "Hot Oil",
                    subtitle: "$15.00"
                },
                {
                    src: "straight_razor_dark.png",
                    title: "Straight Razor",
                    subtitle: "$30.00"
                }
            ],
            reviews: [
                {
                    subtitle: "Lorem ipsum dolor sit argumets, consectterut adipiscing elit Morbi mollis elefeind ante ut asgittis. Sed sodales urna et imperdiet",
                    src: "avadabarbers-trimcut-gallery6.jpg",
                    title: "John Doe"
                },
                {
                    subtitle: "Lorem ipsum dolor sit argumets, consectterut adipiscing elit Morbi mollis elefeind ante ut asgittis. Sed sodales urna et imperdiet",
                    src: "avadabarbers-trimcut-gallery7.jpg",
                    title: "Pete Jones"
                },
                {
                    subtitle: "Lorem ipsum dolor sit argumets, consectterut adipiscing elit Morbi mollis elefeind ante ut asgittis. Sed sodales urna et imperdiet",
                    src: "avadabarbers-trimcut-gallery3.jpg",
                    title: "Mark Wilson"
                }
            ],
            blogs: [
                {
                    src: "avadabarbers-second-blog-320x202.jpg",
                    title: "Avada Barbers Now Open",
                    subtitle: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Consequatur facilis necessitatibus blanditiis veniam magnam amet assumenda"
                },
                {
                    src: "avadabarbers-choosing-blog-320x202.jpg",
                    title: "Choosing The Right Barber",
                    subtitle: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Consequatur facilis necessitatibus blanditiis veniam magnam amet assumenda"
                },
                {
                    src: "avadabarbers-ourservice-blog-320x202.jpg",
                    title: "Quick Service Guide",
                    subtitle: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Consequatur facilis necessitatibus blanditiis veniam magnam amet assumenda"
                }
            ],
            info: ["Avada Barbers", "123 New York Street", "New York City", "info@yourwebsite.com", "+1 (555) 555-1212"],
            socials: ["fa-brands fa-facebook-f", "fa-brands fa-twitter", "fa-brands fa-youtube", "fa-brands fa-instagram"],
            credits: ["Copyright 2012 - 2020 |", "Avada Theme by ThemeFusion |", "All Rights Reserved |", "Powered by WordPress"]
        }
    },
    methods: {
        getImgUrl(imgName) {
            return new URL(`../assets/${imgName}`, import.meta.url).href;
        }
    },
    created() {
        // console.log(this.actions[1].lists[0].info);
    }
}
</script>

<template>
    <main>
        <!-- AWARD SECTION -->
        <section class="award">
            <div class="award-content text-center">
                <h4 class="gold-subtitle">AWARD WINNING</h4>
                <h2 class="silver-title">Pro Barbers</h2>
                <a class="award-btn ms-btn" href="">MEET YOUR NEW BARBER</a>
            </div>
        </section>
        <!-- /AWARD SECTION -->

        <!-- SERVICES SECTION -->
        <section class="services text-center p-5">
            <div class="ms-container-small">
                <h4 class="gold-subtitle">MENS GROOMING</h4>
                <h2 class="silver-title">Services</h2>
                <div class="row row-cols-3">
                    <AppCard v-for="(service, index) in services" id="index" :imgSrc="service.src" :title="service.title" :subtitle="service.subtitle"/>
                </div>
                <a class="service-btn ms-btn" href="">READ ABOUT OUR SERVICES</a>
            </div>
        </section>
        <!-- /SERVICES SECTION -->

        <!-- PRODUCTS SECTION -->
        <section class="products text-center">
            <div class="ms-container-md">
                <h4 class="gold-subtitle">WE HAVE YOU COVERED</h4>
                <h2 class="silver-title">Avada Grooming Products</h2>
                <div class="row row-cols-4">
                    <AppCard v-for="(product, index) in products" id="index" :imgSrc="product.src" :title="product.title" :subtitle="product.subtitle"/>
                </div>
                <a class="products-btn ms-btn" href="">SHOP OUR PRODUCT RANGE</a>
            </div>
        </section>
        <div class="ms-container-small">
            <div class="featured-product">
                <div class="row">
                    <div class="col-4">
                        <div class="left-col">
                            <img src="../assets/shaving_butter.png" alt="">
                        </div>
                    </div>
                    <div class="col-8">
                        <div class="right-col">
                            <h4 class="gold-subtitle">THIS MONTHS FEATURED PRODUCT</h4>
                            <h2 class="silver-title">Shaving Butter</h2>
                            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Consequatur facilis necessitatibus blanditiis veniam magnam amet assumenda, aspernatur optio! Vitae reiciendis doloribus sunt et. Dolorum laboriosam illo laborum porro cupiditate fugiat!</p>
                            <a href="" class="products-btn ms-btn">BUY NOW</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- /PRODUCTS SECTION -->

        <!-- REVIEWS SECTION -->
        <section class="review text-center p-5">
            <div class="ms-container-small">
                <h4 class="gold-subtitle">WHAT PEOPLE SAY</h4>
                <h2 class="silver-title">Reviews</h2>
                <div class="row row-cols-3">
                    <ReviewCard v-for="(review, index) in reviews" id="index" :imgSrc="review.src" :title="review.title" :subtitle="review.subtitle"/>
                </div>
            </div>
        </section>
        <!-- /REVIEWS SECTION -->

        <!-- BLOG SECTION -->
        <section class="blog text-center">
            <div class="ms-container-small">
                <h4 class="gold-subtitle">TALES FROM THE BARBER SHOP</h4>
                <h2 class="silver-title">Recent Blog Posts</h2>
                <div class="row row-cols-3">
                    <AppCard v-for="(blog, index) in blogs" id="index" :imgSrc="blog.src" :title="blog.title" :subtitle="blog.subtitle"/>
                </div>
                <a class="blog-btn ms-btn" href="">READ MORE FROM OUR BLOG</a>
            </div>
        </section>
        <!-- /BLOG SECTION -->

        <!-- FOOTER -->
        <footer>
            <div class="footer-top text-center">
                <div class="ms-container-xs">
                    <div class="row row-cols-3">
                        <div class="col">
                            <div class="inner-col">
                                <img src="../assets/avadabarbers_footer_shop_image.png" alt="">
                                <a class="ms-btn-small" href="">SHOP OUR RANGE NOW</a>
                            </div>
                        </div>
                        <div class="col">
                            <img src="../assets/avadabarbers-logo-x1.png" alt="">
                            <ul class="info-list">
                                <li v-for="(singleInfo, index) in info">
                                    {{singleInfo}}
                                </li>
                            </ul>
                            <h4 class="gold-subtitle">FOLLOW US</h4>
                            <ul class="socials-list">
                                <li v-for="(social, index) in socials">
                                    <i :class="social"></i>
                                </li>
                            </ul>
                        </div>
                        <div class="col">
                            <div class="inner-col">
                                <img src="../assets/avadabarbers_footer_appointment_image.png" alt="">
                                <a class="ms-btn-small" href="">BOOK YOUR APPOINTMENT</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <div class="credits">
                    <p v-for="(credit, index) in credits">{{credit}}</p>
                </div>
            </div>
        </footer>
        <!-- /FOOTER -->
    </main>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;
@use "../styles/partials/variables.scss" as *;

    main {
        // AWARD SECTION
        .award {
            height: 500px;
            background-image: url(../assets/avadabarbers-about-introbackground.jpg);
            background-size: cover;
            clip-path: polygon(0 0, 100% 0, 100% 50%, 100% 100%, 50% 85%, 0 100%);
            display: flex;
            justify-content: center;
            align-items: center;

            .silver-title {
                margin: 1rem 0;
            }

            .award-btn {
                padding: 1rem 1.5rem;
            }
        }
        // /AWARD SECTION

        // SERVICES SECTION
        // /SERVICES SECTION

        // PRODUCTS SECTION
        .products {
            background-image: url(../assets/avadabarbers-reviewsbackground.jpg);
            background-size: cover;
            background-position: center;
            clip-path: polygon(0 10%, 50% 0, 100% 10%, 100% 100%, 50% 100%, 0 100%);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .featured-product {
            border-top: 5px solid $gold-text;
            position: relative;
            bottom: 50px;

            .row > * {
                padding: 0;
            }

            .left-col {
                background-image: url(../assets/avadabarbers-cta-background.jpg);
                background-size: cover;
                height: 400px;
            }

            .right-col {
                background-color: $bg-black-2;
                padding: 2rem;
                height: 400px;

                p {
                    color: $grey-text;
                }
            }
        }
        // /PRODUCTS SECTION

        // BLOG SECTION
        .blog {
            background-color: #f5f5f5;
            clip-path: polygon(0 0, 50% 10%, 100% 0, 100% 100%, 50% 100%, 0 100%);
            padding: 8rem;
        }
        // /BLOG SECTION

        // FOOTER TOP
        .footer-top {
            padding: 3rem;
            background-color: $bg-black-2;
            color: $grey-text;

            .socials-list {
                display: flex;
                justify-content: space-around;
            }
        }

        .footer-bottom {
            background-color: #161718;

            padding: 3rem;

            .credits {
                display: flex;
                justify-content: center;
                align-items: center;
                color: $grey-text;
            }
        }
    }
</style>