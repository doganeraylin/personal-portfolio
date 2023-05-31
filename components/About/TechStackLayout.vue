<template>
    <div class="container">
        <div class="container__blue"></div>
        <div class="container__top_transparent"></div>
        <div class="container__title">
            <h1>tech stack</h1>
        </div>
        <div class="container__right_transparent"></div>
        <div class="container__left_transparent"></div>
        <div class="container__description">  
            <p>Explore the technologies I utilize to create engaging frontend experiences.</p>
        </div>
        <div class="container__yellow"></div>
    </div>
</template>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.container {
    display: grid;
    grid-template-columns: repeat(8, 1fr);
    > * {
        border: 2px solid $black;
    }
    &__blue {
        grid-column: 1 / 2;
        background-color: $primary-blue;
    }
    &__top_transparent {
        grid-column: 2 / 8;
    }
    &__title {
        grid-column: 2 / 8;
        padding: 2rem 1rem;
        font-size: 2.5rem;
    }
    &__right_transparent {
        grid-column: 8 / 9;
    }
    &__left_transparent {
        grid-column: 1 / 2;

    }
    &__description {
        grid-column: 2 / 8;
        padding: 3rem 1rem;
        font-size: 2.5rem;
    }
    &__description p {
        max-width: 90%;
    }
    &__yellow {
        grid-column: 8 / 9;
        background-color: $primary-yellow;
    }


}


</style>