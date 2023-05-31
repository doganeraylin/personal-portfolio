<template>
    <div class="container">
        <div class="container__title">
            <h1>journey through projects</h1>
        </div>
        <div class="container__transparent_square"></div>
        <div class="container__black"></div>
        <div class="container__transparent_horizontal"></div>
        <div class="container__description">
            <p>Explore a collection of my diverse web development projects, showcasing my expertise.</p>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@import "@/styles/variables.scss";

.container {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    > * {
        border: 2px solid $black;
    }
    &__title {
        grid-column: 1 / 3;
        grid-row: 1 / 3;
        background-color: $primary-yellow;
    }
    &__title h1 {
        padding: 2rem;
        font-size: 5rem;
        line-height: 6rem;
        max-width: 70%;
    }

    &__transparent_square {
        grid-column: 3 / 4;
    }
    &__black {
        grid-column: 4 / 5;
        background-color: $black;
    }
    &__transparent_horizontal {
        grid-column: 3 / 5;
    }
    &__description {
        grid-column: 1 / 5;
        text-align: center;
        padding: 2rem;
        font-size: 4rem;
    }
    &__description p {
        max-width: 85%;
        margin: 0 auto;
    }
}
</style>