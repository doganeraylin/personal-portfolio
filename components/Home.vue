<template>
    <div class="container">
        <div class="container__red"></div>
        <div class="container__left_transparent_short"></div>
        <div class="container__left_transparent_long"></div>
        <div class="container__content">
            <h1 class="container__name">Aylin Doğaner</h1>
            <h2 class="container__position">Frontend Developer</h2>
            <p class="container__description">I'm a self-taught frontend developer passionate about creating engaging user experiences through innovative designs and seamless interactions. I aim to combine technical proficiency with a keen eye for aesthetics to bring digital projects to life. Let's collaborate and create something amazing together!</p>
        </div>
        <div class="container__button">
            <Button 
                buttonClass="button_secondary"
                buttonText="explore my work"
                to="/projects"
            />
        </div>
        <div class="container__bottom"></div>
    </div>
</template>


<style lang="scss" scoped>
@import "@/styles/variables.scss";

.container {
    display: grid;
    grid-template-columns: repeat(8, 1fr);
    > * {
        border: 2px solid black;
    }
    &__red {
        background-color: $primary-red;
    }
    &__left_transparent_short,
    &__left_transparent_long {
        display: none;
    }
    &__content {
        grid-column: 2 / 9;
        padding: 1rem;
        background-color: $primary-yellow;
    }
    &__button {
        grid-column: 1 / 6;
        padding: 1rem 0;
    }
    &__bottom {
        background-color: black;
        grid-column: 6 / 9;
    }
    &__name {
        font-size: 3rem;
    }
    &__position {
        line-height: 4rem;
        font-style: italic;
        font-weight: 100;
    }
    &__description {
        margin: 1rem 0;
        line-height: 1.5;
        max-width: 90%;
    }
}


@media (min-width: 768px) {
    .container {
        &__left_transparent_short,
        &__left_transparent_long {
            display: block;
        }
        &__bottom {
            display: none;
        }
        &__red {
            grid-column: 1 / 3;
            grid-row: 1 / 4;
        }
        &__content {
            grid-column: 4 / 9;
        }
        &__button {
            grid-column: 1 / 5;
        }
        &__left_transparent_short {
            grid-column: 5 / 9;
            grid-row: 4 / 5;
            background-color: $black;
        }
        &__name {
            font-size: 4rem;
        }
        &__position {
            font-size: 2.5rem;
            line-height: 4rem;
        }
        &__description {
            font-size: 1.5rem;
            margin: 1rem 0;
            line-height: 1.5;
            max-width: 95%;
        }
    }
}

@media (min-width: 1200px) {
    .container {
        &__content {
            padding: 0 2rem 0;
        }
        &__name {
            font-size: 7rem;
        }
        &__position {
            font-size: 4rem;
            line-height: 7rem;
            font-style: italic;
            opacity: 0.5;
        }
        &__description {
            font-size: 2rem;
            margin: 1rem 0;
            line-height: 1.5;
            max-width: 95%;
        }
    }
}
</style>