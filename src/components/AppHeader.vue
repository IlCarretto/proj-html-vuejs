<script>
export default {
    name: "AppHeader",
    data() {
        return {

        }
    }
}
</script>

<template>
    <header>
        <div class="ms-container-small">
            <div class="header-top">
                <div class="logo-container">
                    <img src="../assets/avadabarbers-logo-x1.png" alt="">
                </div>
                <div class="icons-container">
                    <i class="fa-solid fa-cart-shopping"></i>
                    <i class="fa-solid fa-bars"></i>
                </div>
            </div>
            <div class="header-bottom">
                <div class="text-content">
                    <h1 class="header-title">Barber Shop</h1>
                    <div class="line"></div>
                    <p class="header-subtitle">The Pinnacle of Male Grooming</p>
                    <a class="ms-btn" href="">LEARN MORE</a>
                </div>
                <div class="img-content">
                    <img src="../assets/avadabarbers_hero_focalmirror.png" alt="">
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables.scss" as *;

    header {
        height: 100vh;
        background-image: url(../assets/avadabarbers-homepage-hero-bg.jpg);
        background-size: cover;
        
        .header-top {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 2rem;

            .icons-container {
                color: white;
                
                .fa-bars {
                    padding-left: 1rem;
                    font-size: 1.6rem;
                }
            }
        }

        .header-bottom {
            display: flex;
            justify-content: space-between;
            align-items: center;

            .text-content {
                
                .header-title {
                    color: $silver-text;
                    font-size: 5rem;
                    font-family: "Abril Fatface";
                }
                
                .line {
                    background-color: $gold-text;
                    width: 200px;
                    height: 4px;
                    margin: 1rem 0;
                }

                .header-subtitle {
                    color: $grey-text;
                    font-size: 1.4rem;
                    margin: 1rem 0;
                }
                
                a {
                    margin: 1rem 0;
                }
            }
            .img-content {
                width: 60vh;
            }

        }
    }
</style>