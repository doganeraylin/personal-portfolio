<template>
    <div class="container">
        <div class="container__text">
            <p>
                Explore a collection of my diverse web development projects, showcasing my expertise in crafting user-friendly interfaces and pushing the boundaries of frontend innovation.
            </p>
        </div>
        <div class="container__transparent_vertical"></div>
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
        grid-column: span 4;
        padding: 2.5rem 1.5rem; 
        background-color: $primary-red;
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