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
    methods: {
        // FUNZIONE CHE ATTIVA L'ELEMENTO DEL MENU con hover
        activeMenuItem(index) {
            this.menuItem[index].active = true;
        },

        // FUNZIONE CHE DISATTIVA L'ELEMENTO DEL MENU
        inActiveMenuItem(index) {
            this.menuItem[index].active = false;
        }
    }
}

</script>

<template>
    <header>
        <!-- Container -->
        <div class="container">
            <!-- Row -->
            <div class="row">
                <!-- Logo Col -->
                <div class="col">
                    <img src="../assets/dc-logo.png" alt="">
                </div>
                <!-- Menu Col -->
                <div class="col">
                    <!-- Header Menu -->
                    <ul>
                        <li v-for="(item, index) in menuItem" :key="index" :class=" item.active ? 'active' : '' " @mouseover="activeMenuItem(index)" @mouseleave="inActiveMenuItem(index)">
                            <a :href="item.link" v-text="item.label"></a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;

    header {
        height: 120px;

        .row {
            justify-content: space-between;

            .col {
                height: 100%;
                display: flex;
                align-items: center;

                img {
                    width: 80%;
                    cursor: pointer;
                }

                ul {
                    height: 100%;
                    display: flex;
                    align-items: center;
                }

                li {
                    display: flex;
                    align-items: center;
                    height: 100%;
                    font-size: 14px;
                    font-weight: 700;
                    padding: 15px;
                    border-bottom: 5px solid transparent;
                    cursor: pointer;
                }
                .active {
                    color: #0282F9;
                    border-bottom-color: #0282F9;
                }
            }
        }
    }   
</style>