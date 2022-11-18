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
            ]
        }
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
        <section class="services text-center">
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
        <section class="review text-center">
            <div class="ms-container-small">
                <h4 class="gold-subtitle">WHAT PEOPLE SAY</h4>
                <h2 class="silver-title">Reviews</h2>
                <div class="row row-cols-3">
                    <ReviewCard v-for="(review, index) in reviews" id="index" :imgSrc="review.src" :title="review.title" :subtitle="review.subtitle"/>
                </div>
            </div>
        </section>
        <!-- /REVIEWS SECTION -->
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

        // PRODUCTS SECTION
        .products {
            background-image: url(../assets/avadabarbers-reviewsbackground.jpg);
            background-size: cover;
            background-position: center;
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
    }
</style>