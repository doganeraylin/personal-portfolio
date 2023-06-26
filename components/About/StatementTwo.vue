<template>
    <div class="container">
        <div class="container__text">
            <p>
               I am eager to collaborate with a team of like-minded individuals who share a passion for pushing the boundaries of design and frontend development. 
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
        background-color: $primary-yellow;
    }
}

@media (min-width: 768px) {
    .container {
        &__text {
            font-size: 1.75rem;
            line-height: 2.25rem;
            padding: 3.5rem 1.5rem; 
        }
    }
}

</style>