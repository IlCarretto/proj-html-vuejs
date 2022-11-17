<script>
import AppCard from './AppCard.vue';

export default {
    name: "AppMain",
    components: {
        AppCard
    }, 
    data() {
        return {
            services: [
                {
                    src: "../assets/avadabarbers-trimcut-icon-before.png",
                    title: "Trim & Cut",
                    subtitle: "Avada Barbers are experts in the lickety split trim and hair cut. Quick but careful and ridiulously good looking."
                },
                {
                    src: "../assets/avadabarbers-washndry-icon.png",
                    title: "Wash & Dry",
                    subtitle: "Take a seat in our fine leather chairs, lean back and let us lather you a fresh head in a luxurious fashion."
                },
                {
                    src: "../assets/avadabarbers-beardtrim-icon.png",
                    title: "Beard Tidy",
                    subtitle: "Tame the tangles and untidy facial hairs like a gentleman with our Beard Tidy services from Avada Barbers."
                },
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

        // SERVICES SECTION
        .services {
        }
        // /SERVICES SECTION
    }
</style>