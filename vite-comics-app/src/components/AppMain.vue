<script>
export default {
    data() {
        return {

        }
    },
}
</script>

<template lang="">
    <main>
        <!-- Container -->
        <div class="container">
            <!-- Row -->
            <div class="row">
                <!-- Content -->
                <h1> --> Content goes here &lt;--</h1>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;

main {
    height: 150px;
    background-color: #1C1C1C;
    color: $primaryColor;

    .container {
        max-width: 1600px;
        margin: 0 auto;
        height: 100%;

        .row {
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
        }
    }
}
</style>