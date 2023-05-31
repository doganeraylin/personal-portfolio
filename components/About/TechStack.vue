<template>
    <div class="container">
        <div class="tech_stack">
            <img src="/react.png">
            <p>Next.js</p>
        </div>
        <div class="tech_stack">
            <img src="/react.png">
            <p>Next.js</p>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@import "@/styles/variables.scss";

.container {
    display: flex;
    justify-content: space-around;
    gap: 1rem;
}

.tech_stack {
    border: 1px solid $black;
    text-align: center;
    padding: 1rem;
    img {
        max-width: 150px;
    }
    p {
        font-size: 1.5rem;
        opacity: 0.5;
        margin: 0.5rem;
    }
}
</style>