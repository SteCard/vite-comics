<script>

import AppMainCard from './AppMainCard.vue';

export default {
    components: {
        // DICHIARO APP_MAIN_CARD
        AppMainCard
    },
    data() {
        return {
            cardItem: [
                {
                    thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    price: "$19.99",
                    series: "Action Comics",
                    type: "comic book",
                },
                {
                    thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    price: "$3.99",
                    series: "American Vampire 1976",
                    type: "comic book",
                },
                {
                    thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    price: "$16.99",
                    series: "Aquaman",
                    type: "graphic novel",
                },
                {
                    thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    price: "$2.99",
                    series: "Batgirl",
                    type: "comic book",
                },
                {
                    thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    price: "$3.99",
                    series: "Batman",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    price: "$2.99",
                    series: "Batman Beyond",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    price: "$3.99",
                    series: "Batman/Superman",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    price: "$4.99",
                    series: "Batman/Superman Annual",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    price: "$5.99",
                    series: "Batman: The Joker War Zone",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    price: "$6.99",
                    series: "Batman: Three Jokers",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    price: "$4.99",
                    series: "Batman: White Knight Presents: Harley Quinn",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    price: "$16.99",
                    series: "Catwoman",
                    type: "graphic novel",
                },
            ]
        }
    },
}
</script>

<template lang="">
    <main>
        <!-- Jumbotron Container Fluid -->
        <div class="container-fluid jumbotron-container">
        <!-- Jumbotron Container -->
            <div class="container">
                <!-- Jumbotron Row -->
                <div class="jumbotron-row">
                    <!-- Jumbotron Col -->
                    <div class="jumbotron-col">
                        <!-- Jumbtron Label -->
                        <h1>CURRENT SERIES</h1>
                    </div>
                </div>
            </div>
        </div>
        <!-- Main Content Card Container -->
        <div class="container">
            <!-- Main Content Row -->
            <div class="row">
                <AppMainCard  v-for="(card, index) in cardItem" :key="index" :thumb="card.thumb" :series="card.series"/>
                <!-- Main Load Button Col -->
                <div class="load-col">
                    <a href="">LOAD MORE</a>
                </div>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

main {
    background-color: #1C1C1C;
    color: $primaryColor;

    .jumbotron-container {
        height: 45vh;
        background-image: url(../assets/jumbotron.jpg);
        background-size: cover;
        position: relative;

        h1 {
            padding: 15px 30px;
            font-size: 25px;
            background-color: $secondaryColor;
            position: absolute;
            bottom: -30px;
        }
    }

    .container {
        padding: 50px 0;

        .row {
            justify-content: center;
            flex-wrap: wrap;

            .load-col {
                margin-top: 50px;

                a {
                    padding: 12px 65px;
                    font-weight: 700;
                    background-color: $secondaryColor;
                }
            }
        }
    }
}
</style>