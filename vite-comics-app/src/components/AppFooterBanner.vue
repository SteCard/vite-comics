<!-- SCRIPT VUE.JS -->
<script>
export default {
    data() {
        return {
            bannerItem: [
                {
                    label: 'DIGITAL COMICS',
                    src: '/src/assets/buy-comics-digital-comics.png',
                },
                {
                    label: 'DC MERCHANDISE',
                    src: '/src/assets/buy-comics-merchandise.png',
                },
                {
                    label: 'SUBSCRIPTION',
                    src: '/src/assets/buy-comics-subscriptions.png',
                },
                {
                    label: 'COMICS SHOP LOCATOR',
                    src: '/src/assets/buy-comics-shop-locator.png',
                },
                {
                    label: 'DC POWER VISA',
                    src: '/src/assets/buy-dc-power-visa.svg',
                },
            ]
        }
    },
}
</script>

<template lang="">
    <!-- Banner Container Fluid -->
    <div class="container-fluid banner-container">
        <!-- Banner Container -->
        <div class="container">
            <!-- Row -->
            <div class="row">
                <!-- Col -->
                <div class="banner-col" v-for="(item, index) in bannerItem" :key="index">
                    <img :src="item.src" :alt="`banner-image-${index+1}`">
                    <span v-text="item.label"></span>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

.banner-col {
    display: flex;
    justify-content: center;
    align-items: center;
    width: calc(100% / 5 - 40px);
    margin: 0 20px;
    height: 100%;

    img {
        width: 20%;

        &:hover {
            filter: invert(100%);
        }
    }

    span {
        margin-left: 20px;
        font-size: 15px;

        &:hover {
            color: black;
            font-weight: 700;
        }
    }

    img,
    span {
        cursor: pointer;
    }
}

.banner-container {
    background-color: $secondaryColor;

    .container {
        padding: 40px 0;

        .row {
            align-items: center;
        }
    }
}
</style>