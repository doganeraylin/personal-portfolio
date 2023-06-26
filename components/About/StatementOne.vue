<template>
    <div class="container">
        <div class="container__text">
            <p> I believe that combining technical proficiency with a keen eye for aesthetics and user experience is key to crafting exceptional digital experiences. </p>
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
            border: 2px solid black;
        }
        &__text {
            padding: 2.5rem 1.5rem; 
            background-color: $primary-red;
            color: $primary-gray;
            grid-column: span 4;
        }
        &__text p {
            max-width: 85%;
        }
        &__transparent_horizontal_first {
            grid-column: 1 / 3;
        }
        &__transparent_horizontal_second {
            grid-column: 3 / 5;
            padding: 2rem;
        }
        &__black {
            background: $black;
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