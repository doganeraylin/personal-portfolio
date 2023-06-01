<template>
    <div class="container">
        <div class="container__top_horizontal"></div>
        <div class="container__left_yellow"></div>
        <div class="container__left_transparent"></div>
        <div class="container__video">video</div>
        <div class="container__right_yellow"></div>
        <div class=" container__bottom_horizontal"></div>
    </div>
</template>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.container {
    display: grid;
    grid-template-columns: repeat(9, 1fr);
    grid-template-rows: repeat(7, 0.5fr);
    > * {
        border: 2px solid $black;
    }
    &__top_horizontal {
        grid-column: span 10;
    } 
    &__left_yellow {
        grid-column: 1 / 2;
        grid-row: 2 / 5;
        background-color: $primary-yellow;
    }
    &__left_transparent {
        grid-column: 1 / 2;
        grid-row: 5 / 8;
    }
    &__video {
        grid-column: 2 / 9;
        grid-row: 2 / 8;
        padding: 4rem;
    }
    &__right_yellow {
        grid-column: 9 / 10;
        grid-row: 2 / 8;
        background-color: $primary-yellow;
    }
    &__bottom_horizontal {
        grid-column: 1 / 10;
        grid-row: 7 / 8;
    }

}
</style>