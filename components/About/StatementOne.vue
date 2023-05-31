<template>
    <div class="container">
        <div class="container__text">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse vestibulum molestie quam ac dapibus. Donec ut leo fermentum, placerat velit.</p>
        </div>
        <div class="container__transparent_vertical"></div>
        <div class="container__transparent_horizontal_first"></div>
        <div class="container__transparent_horizontal_second"></div>
        <div class="container__black"></div>
    </div>
</template>

<style lang="scss" scoped>
@import "@/styles/variables.scss";


.container {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
        > * {
            border: 3px solid black;
        }
        &__text {
            padding: 5rem;
            background-color: $primary-yellow;
            grid-column: span 4;
            font-size: 2rem;
        }

        &__text p {
            max-width: 90%;
        }
        &__transparent_horizontal_first {
            grid-column: 1 / 3;
            padding: 2rem;
        }
        &__transparent_horizontal_second {
            grid-column: 3 / 5;
            padding: 2rem;
        }
        &__black {
            background: $black;
        }
}
</style>