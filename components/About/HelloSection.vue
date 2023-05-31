<template>
    <div class="container">
        <div class="empty_boxes">
            <div class="empty_boxes__top_left"></div>
            <div class="empty_boxes__red"></div>
            <div class="empty_boxes__top_right"></div>
            <div class="empty_boxes__yellow"></div>
            <div class="empty_boxes__bottom_center"></div>
            <div>
                <div class="empty_boxes__bottom_transparent"></div>
                <div class="empty_boxes__black"></div>
            </div>

        </div>
        <div class="intro_container">
            <h1>hello!</h1>
            <p>My name is Aylin, and I am a passionate junior frontend developer. I am enthusiastic about creating engaging and user-friendly web experiences through clean and efficient code.</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@import "@/styles/variables.scss";
 
    .container {
        display: grid;
        grid-template-columns: repeat(6, 1fr);
        grid-template-rows: 1fr;
        > * {
            border: 1px solid $black;
        }
    }
    .empty_boxes {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        > * {
            border: 1px solid $black;
        }
        &__top_left {
            padding: 4rem;
            grid-row: 1 / 2; 
        }
        &__red {
            padding: 4rem;
            background-color: $primary-red;
            grid-column: 2 / 3;
        }
        &__top_right {
            padding: 4rem;
            grid-column: 3 / 4;
        }
        &__yellow {
            grid-column: 1 / 2;
            grid-row: 2 / 3;
            padding: 7rem 4rem;
            background-color: $primary-yellow;
        
        }
        &__bottom_center {
            padding: 7rem 4rem;
        }
        &__bottom_transparent {
            padding: 4rem;
        }
        &__black {
            background-color: $black;
        }
        
    }
    .intro_container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        grid-column: 2 / 7;
        color: $primary-gray;
        background-color: $primary-blue;
        padding: 1rem;
        h1 {
            font-size: 8rem;
        }
        p {
            max-width: 600px;
            line-height: 2rem;
            font-size: 1.5rem;
            margin: 1rem 0;
        }
    }   








</style>