<template>
    <div class="container">
        <div class="container__top_horizontal"></div>
        <div class="container__left_yellow"></div>
        <div class="container__title">
            <h1>project details</h1>
        </div>
        <div class="container__top_blue"></div>
        <div class="container__top_transparent"></div>
        <!-- <div class="container__left_transparent"></div> -->
        <div class="container__red"></div>
        <div class="container__description">
            <ul>
                <li>Provide more specific details about the project, such as the technologies you used (e.g., programming.</li>
                <li>Provide more specific details about the project, such as the technologies you used (e.g., programming.</li>
                <li>Provide more specific details about the project, such as the technologies you used (e.g., programming.</li>
                <li>Provide more specific details about the project, such as the technologies you used (e.g., programming.</li>
                <li>Provide more specific details about the project, such as the technologies you used (e.g., programming.</li>
                <li>Provide more specific details about the project, such as the technologies you used (e.g., programming.</li>
                <li>Provide more specific details about the project, such as the technologies you used (e.g., programming.</li>
                
            </ul>
        </div>
        <!-- <div class="container__right_horizontal_transparent"></div> -->
        <div class="container__right_yellow"></div>
        <div class="container__bottom_blue"></div>
        <!-- <div class="container__red"></div> -->
        <div class="container__bottom_horizontal"></div>
    </div>
</template>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.container {
    display: grid;
    grid-template-columns: repeat(9, 1fr);
    grid-template-rows: repeat(6, 0.1fr);
    > * {
        border: 2px solid $black;
    }
    &__top_horizontal {
        grid-column: 1 / 10;
        padding: 1rem;
    }
    &__left_yellow {
        grid-column: 1 / 4;
        background-color: $primary-yellow;
    }
    &__title {
        grid-column: 4 / 8;
        padding: 1rem;
    }
    &__top_blue {
        grid-column: 8 / 9 ;
        background-color: $primary-blue;
    }
    &__top_transparent {
        grid-column: 9 / 10;;
    }
    &__description {
        grid-column: span 10;
        padding: 1.5rem 3rem;
    }
    &__description ul {
        list-style: none;
        line-height: 1.5rem;
    }
    &__description ul li {
        margin: 0.5rem 0;
    }
    &__left_blue,
    &__right_horizontal_transparent,
    &__right_yellow,
    &__right_vertical_transparent,
    &__red {
        display: none;
    }
    &__bottom_horizontal {
        grid-column: span 10;
    }
}

@media (min-width: 768px) {
    .container {
        &__red,
        &__right_horizontal_transparent,
        &__right_yellow,
        &__right_vertical_transparent,
        &__red {
            display: block;
        }
        &__red {
            grid-column: 1 / 2;
            grid-row: 3 / 7;
            background-color: $primary-red;
        }
        &__description {
            grid-column: 2 / 9;
        }
        &__description ul {
               max-width: 65vw;
        }
        &__right_yellow {
            grid-column: 9 / 10;
            grid-row: 3 / 7;
            background-color: $primary-yellow;
        }
        &__bottom_blue{
            grid-column: 2 / 9;
            grid-row: 4 / 7;
            background-color: $primary-blue;
        }
        &__title {
            text-transform: uppercase;
        }
    }
}
</style>