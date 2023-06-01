<template>
    <div class="container">
        <div class="container__black"></div>
        <div class="container__title">
            <h1>space tourism website</h1>
        </div>
        <div class="container__red"></div>
        <div class="container__left_transparent"></div>
        <div class="container__links">
            <ul>
                <li><NuxtLink to="">https://github.com/doganeraylin?tab=repositories</NuxtLink></li>
                <li><NuxtLink to="">https://github.com/doganeraylin?tab=repositories</NuxtLink></li>
            </ul>
        </div>
        <div class="container__right_transparent"></div>
    </div>
</template>


<style lang="scss" scoped>
@import "@/styles/variables.scss";
.container {
    display: grid;
    grid-template-columns: repeat(9, 1fr);
        grid-template-rows: repeat(4, 1fr);
    text-align: center;
    > * {
        border: 1px solid black;
    }

    &__black {
        grid-column: 1 / 2;
        background-color: $black;
    }
    &__title,
    &__links {
        grid-column: 2 / 9;
    }
    &__title {
        padding: 1rem;
    }
    &__links {
        display: flex;
        align-items: center;
        justify-content: center;
        grid-row: 2 / 5;
    }
    &__red {
        grid-column: 9 / 10;
        background-color: $primary-red;
    }
    &__links ul {
        list-style: none;
    }
    &__left_transparent,
    &__right_transparent {
        grid-row: 2 / 5;
    }
    &__right_transparent {
        grid-column: 9 / 10;
    }
}

@media (min-width: 992px) {
    .container {
        &__title {
            padding: 2rem;
            text-transform: uppercase;
        }
    }
}
</style>