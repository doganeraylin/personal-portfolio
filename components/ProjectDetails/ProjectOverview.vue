<template>
    <div class="container">
        <div class="container__red"></div>
        <div class="container__title">
            <h1>project overview</h1>
        </div>
        <div class="container__black"></div>
        <div class="container__description">
            <p>Start with a brief introduction or overview of the project. Mention its purpose, goals, and any unique features or challenges you encountered.Start with a brief introduction or overview of the project. Mention its purpose, goals, and any unique features or challenges you encountered.</p>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@import "@/styles/variables.scss";

.container {
    display: grid;
    grid-template-columns: repeat(9, 1fr);
    text-align: center;
    > * {
        border: 2px solid $black;
    }
    &__red {
        grid-column: 1 / 2;
        background-color: $primary-red;
    }
    &__title {
        grid-column: 2 / 9;
        font-size: 0.9rem;
        padding: 1rem;
    }
    &__black {
        grid-column: 9 / 10;
        background-color: $black;
    }
    &__description {
        grid-column: 1 / 10;
        padding: 2rem;
    }
    &__description p {
        line-height: 1.5rem;
    }
}

@media (min-width: 768px ) {
    .container {
        &__title {
            font-size: 2.5rem;
            text-transform: uppercase;
        }
        &__description {
            padding: 3rem;
        }
        &__description p {
            max-width: 75vw;
            margin: 5rem auto;
            font-size: 1.75rem;
            line-height: 2.25rem;
        }
    }
}

@media (min-width: 1080px ) {
    .container {
        &__title {
            padding: 4rem;
            font-size: 2.5rem;
            text-transform: uppercase;
        }
        &__description p {
            font-size: 2.5rem;
            line-height: 3.5rem;
        }
    }
}
</style>