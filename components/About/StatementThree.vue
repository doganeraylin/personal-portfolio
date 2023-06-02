<template>
    <div class="container">
        <div class="container__left_vertical_thick"></div>
        <div class="container__top_horizontal"></div>
        <div class="container__yellow"></div>
        <div class="container__left_vertical-thin"></div>
        <div class="container__text">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse vestibulum molestie quam ac dapibus. Donec ut leo fermentum, placerat velit.</p>
        </div>
        <div class="container__bottom_short"></div>
        <div class="container__bottom_long"></div>
    </div>
</template>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.container {
    display: grid;
    grid-template-columns: repeat(10, 1fr);
    grid-template-rows: repeat(2, 0.4fr);
    color: $primary-gray;
    > * {
        border: 2px solid black;
    }
    &__left_vertical_thick {
        grid-column: 1 / 2;
        grid-row: 1 / 3;
    }
    &__top_horizontal {
        grid-column: 2 / 11;
        grid-row: 1 / 2;
    }
    &__yellow {
        grid-column: 9 / 11;
        grid-row: 1 / 2;
        background-color: $primary-yellow;
    }
    &__text {
        grid-column: 3 / 11;
        grid-row: 2 / 3;
        padding: 2.5rem 1.5rem; 
        background-color: $primary-blue;
    }
    &__bottom_short {
        grid-column: 1 / 4;
        grid-row: 3 / 4;
    }
    &__bottom_long {
        grid-column: 4 / 11;
    }
}

@media (min-width: 768px) {
    .container {
        &__text {
            font-size: 1.75rem;
            line-height: 2.25rem;
            padding: 3.5rem 1.5rem; 
        }
        &__text p {
            max-width: 75%;
        }
    }
}

</style>