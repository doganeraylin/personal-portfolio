<template>
    <div class="container">
        <div class="container__text">Explore a collection of my diverse web development projects, showcasing my expertise in crafting user-friendly interfaces and pushing the boundaries of frontend innovation.</div>
        <div class="container__transparent_vertical"></div>
        <!-- <div class="container__transparent_horizontal"></div> -->
    </div>
</template>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.container {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    > * {
        border: 3px solid black;
    }
    &__text {
        grid-column: span 4;
        padding: 5rem;
        font-size: 2rem;
        background-color: $primary-red;
    }
    // &__transparent_horizontal {
    //     padding: 3rem;
    //     grid-column: span 5;
    // }
}

</style>