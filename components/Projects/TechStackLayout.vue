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
        <div class="container__bottom_transparent"></div>
    </div>
</template>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.container {
    display: grid;
    grid-template-columns: repeat(7, 1fr);
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
        grid-column: 1 / 8;
        padding: 1rem;
        font-size: 1.5rem;
        display: flex;
        align-items: center;
        text-align: center;
        background-color: $primary-red;
    }
    &__left_transparent {
        grid-column: 1 / 2;

    }
    &__description {
        grid-column: 2 / 8;
        padding: 3rem 1rem;
    }
    &__description p {
        max-width: 85%;
        font-size: 2rem;
    }
    &__blue,
    &__top_transparent,
    &__right_transparent,
    &__yellow {
        display: none;
    }
    &__bottom_transparent {
        grid-column: 1 / 8;
        padding: 3rem 0;
    }
}

@media (min-width: 768px) {
    .container {
        grid-template-rows: repeat(4, 0.5fr);
        &__blue,
        &__top_transparent,
        &__right_transparent,
        &__yellow {
            display: block;
        }
        &__top_transparent {
            grid-column: 2 / 8;
        }
        &__title {
            grid-column: 2 / 7;
            padding: 1rem;
            font-size: 1.5rem;
            text-align: center;
            background-color: $primary-red;
        }
        &__right_transparent {
            grid-column: 7 / 8;
        }
        &__left_transparent {
            grid-column: 1 / 2;
            grid-row: 3 / 5;

        }
        &__description {
            grid-column: 2 / 7;
            grid-row: 3 / 5;
            padding: 3rem 1rem;
        }
        &__description p {
            max-width: 80%;
            font-size: 3rem;
        }
        &__yellow {
            grid-column: 7 / 8;
            grid-row: 3 / 5;
            background-color: $primary-yellow;
        }
        &__blue {
            grid-column: 1 / 2;
            grid-row: 1 / 3;
            background-color: $primary-blue;
        }

        &__title {
            text-transform: uppercase;
            text-align: left;
        }
    }   
}


</style>