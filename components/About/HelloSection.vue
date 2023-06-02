<template>
    <div class="container">
        <div class="container__top_left"></div>
        <div class="container__red"></div>
        <div class="container__top_right"></div>
        <div class="container__yellow"></div>
        <div class="container__bottom_center"></div>
        <div class="container__bottom_transparent"></div>
        <div class="container__black"></div>
        <div class="container__content">
            <h1 class="title">hello!</h1>
            <p class="description">My name is Aylin, and I am a passionate junior frontend developer. I am enthusiastic about creating engaging and user-friendly web experiences through clean and efficient code.</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.container {
    display: grid;
    grid-template-columns: repeat(6, 1fr);
    grid-template-rows: repeat(3, 0.5fr);
    > * {
        border: 2px solid black;
    }
 
    &__yellow {
        grid-column: 1 / 2;
        grid-row: 2 / 4;
        background-color: $primary-yellow;
    }
 
    &__content {
        grid-column: 2 / 7;
        grid-row: 1 / 4;
        padding: 1rem;
        color: $primary-gray;
        background-color: $primary-blue;
    }
    // 
    &__red,
    &__bottom_center,
    &__top_right,
    &__bottom_transparent,
    &__black {
        display: none;
    }
 
}
.title {
    font-size: 5rem;
}
.description {
    font-size: 1.25rem;
    line-height: 1.75rem;
    max-width: 80%;
    margin: 2rem 0;
}

@media (min-width: 768px) {
    .container {
        &__red,
        &__bottom_center,
        &__top_right,
        &__bottom_transparent,
        &__black {
            display: block;
        }
        &__content {
            grid-column: 4 / 7;
            grid-row: 1 / 4;
            padding: 1rem;
            color: $primary-gray;
            background-color: $primary-blue;
        }
        &__red {
            background-color: $primary-red;
        }  
        &__bottom_center {
            grid-row: 2 / 4;
        }
        &__black {
            grid-column: 3 / 4;
            background-color: $black;
        }
    }
    .title {
        font-size: 8rem;
    }
    .description {
        font-size: 2rem;
        line-height: 2.5rem;
        max-width: 95%;
        margin: 2rem 0;
    }
}

    // .container {
    //     display: grid;
    //     grid-template-columns: repeat(6, 1fr);
    //     grid-template-rows: 1fr;
    //     > * {
    //         border: 1px solid $black;
    //     }
    // }
    // .container {
    //     display: grid;
    //     grid-template-columns: repeat(3, 1fr);
    //     > * {
    //         border: 1px solid $black;
    //     }
    //     &__top_left {
    //         padding: 4rem;
    //         grid-row: 1 / 2; 
    //     }
    //     &__red {
    //         padding: 4rem;
    //         background-color: $primary-red;
    //         grid-column: 2 / 3;
    //     }
    //     &__top_right {
    //         padding: 4rem;
    //         grid-column: 3 / 4;
    //     }
    //     &__yellow {
    //         grid-column: 1 / 2;
    //         grid-row: 2 / 3;
    //         padding: 7rem 4rem;
    //         background-color: $primary-yellow;
        
    //     }
    //     &__bottom_center {
    //         padding: 7rem 4rem;
    //     }
    //     &__bottom_transparent {
    //         padding: 4rem;
    //     }
    //     &__black {
    //         background-color: $black;
    //     }
        
    // }
    // .intro_container {
    //     display: flex;
    //     flex-direction: column;
    //     justify-content: center;
    //     grid-column: 2 / 7;
    //     color: $primary-gray;
    //     background-color: $primary-blue;
    //     padding: 1rem;
    //     h1 {
    //         font-size: 8rem;
    //     }
    //     p {
    //         max-width: 600px;
    //         line-height: 2rem;
    //         font-size: 1.5rem;
    //         margin: 1rem 0;
    //     }
    // }   








</style>