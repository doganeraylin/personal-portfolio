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
        grid-column: 1 / 5;
        text-align: center;
        background-color: $primary-yellow;
    }
    &__title h1 {
        font-size: 4rem;
        line-height: 6rem;
        padding: 1rem;
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
        padding: 1rem 0;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
    }
    &__description p {
        max-width: 85%;
        margin: 0 auto;
        font-size: 2rem;
    }
    &__transparent_square,
    &__transparent_horizontal,
    &__black {
        display: none;
    }
}

@media (min-width: 768px) {
    .container {
        grid-template-rows: repeat(3, 0.5fr);
        &__transparent_square,
        &__transparent_horizontal,
        &__black {
            display: block;
        }
        &__title {
        display: flex;
        align-items: center;
        text-align: left;
        grid-column: 1 / 3;
        grid-row: 1 / 3;
        background-color: $primary-yellow;
        }
        &__title h1 {
            max-width: 80%;
            font-size: 5rem;
        }
        &__transparent_horizontal {
            grid-column: 3 / 5;
        }
        &__description {
        padding: 2rem 0;
        font-size: 4rem;
        }
        &__description p {
            max-width: 85%;
            margin: 0 auto;
        }
    }
}
@media (min-width: 1200px) {
    .container {
        &__title h1 {
            max-width: 80%;
            font-size: 8rem;
            line-height: 9.5rem;
        }
        &__description {
            padding: 2rem 0;
        }
        &__description p {
            max-width: 60%;
            font-size: 3rem;
        }
    }
}
</style>