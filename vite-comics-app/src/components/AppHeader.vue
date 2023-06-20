<script>
export default {
    data() {
        return {
            // MENU ARRAY
            menuItem: [
                {
                    label: 'CHARACTERS',
                    link: '#',
                    active: false,
                },
                {
                    label: 'COMICS',
                    link: '#',
                    active: false,
                },
                {
                    label: 'MOVIES',
                    link: '#',
                    active: false,
                },
                {
                    label: 'TV',
                    link: '#',
                    active: false,
                },
                {
                    label: 'GAMES',
                    link: '#',
                    active: false,
                },
                {
                    label: 'COLLECTIBLES',
                    link: '#',
                    active: false,
                },
                {
                    label: 'VIDEOS',
                    link: '#',
                    active: false,
                },
                {
                    label: 'FANS',
                    link: '#',
                    active: false,
                },
                {
                    label: 'NEWS',
                    link: '#',
                    active: false,
                },
                {
                    label: 'SHOP',
                    link: '#',
                    active: false,
                },
            ]
        }
    },
}

</script>

<template lang="">
    <header>
        <!-- Container -->
        <div class="container">
            <!-- Row -->
            <div class="row">
                <!-- Logo Col -->
                <div class="col">
                    <img src="/dc-logo.png" alt="">
                </div>
                <!-- Menu Col -->
                <div class="col">
                    <!-- Header Menu -->
                    <ul>
                        <li v-for="(item, index) in menuItem">
                            <a :href="item.link" v-text="item.label"></a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss">
    
</style>