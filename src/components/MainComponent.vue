<template>
    <main>
        <div class="container  d-flex align-items-center">
        <h3>--> Content goes here <--</h3>
        </div>
    </main>
</template>

<script>
    export default {
        name: 'MainComponent'
    }
</script>

<style lang="scss" scoped>
@use "../assets/styles/partials/variables" as *;

    main {
        font-family: $anton;
        background-color: $main-bg;
        color: $general-white;
        &>div {
            height: 120px;
        }
    }
</style>