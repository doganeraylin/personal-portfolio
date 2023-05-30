<template>
     <Navbar/>
    <div class="wrapper">
        
        <div class="left_container_wrapper">
            <div class="left_container">
                <div class="left_container__red_box"></div>
                <button class="left_container__button">explore my work</button>
            </div>
            <div class="left_container">
                <div class="left_container__box_top"></div>
                <div class="left_container__box_bottom"></div>
            </div>
        </div>
        <div class="right_container">
            <p class="right_container__name">Aylin Doğaner</p>
            <p class="right_container__position">Frontend Developer</p>
            <p class="right_container__description">Based on the information provided, "PP Neue Montreal" does not have a specific retro style. It is primarily a modern sans-serif font. Retro fonts typically have distinctive characteristics from.</p>
            <button class="right_container__button_mobile">explore my work</button>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.wrapper {
    > * {
        border: 2px solid black;
    }
}

.right_container {
    padding: 1rem;
    background-color: $primary-yellow;
        > * {
        padding: 0.5rem;
        }
        &__name {
            font-size: 3rem;
            font-weight: 700;
        }
        &__position {
            font-size: 1.5rem;
            opacity: 0.5;
            font-style: italic;
        }
        &__description {
            line-height: 1.3rem;
            max-width: 70%;
        }
        &__button {
            display: none;
        }
}


@media (min-width: 768px) {
    .wrapper {
        display: flex;

    }
    .left_container_wrapper {
        min-height: 100vh;
        border: 3px solid magenta;
        display: flex;
 
        align-items: flex-start;
        > * {
            border: 2px solid black;
        }
       
    }
    .right_container {
        &__button_mobile {
            display: none;
        }
     
    }
}

.left_container {
    width: 100%;
    height: 100%;
    &__red_box {
        min-width: 300px;
        min-height: 80%;
        background-color: $primary-red;
    }
    &__button {
        border: none;
    }
    &__box_top {
        background-color: orange;
    }
    &__box_bottom {
        background-color: pink;
    }
 
}

// @media (min-width: 768px) {
//     .container {
//         height: 100vh;
//         border: 2px solid $black;
//         display: grid;
//         grid-template-columns: repeat(10, 1fr);

//         &__navbar {
//             grid-column: 1 / 5;
//         }
//         &__introduction {
//             grid-column: 5 / 11;
//             grid-row: 1 / 5;
//             background-color: $primary-yellow;
//             border: 1px solid $black;

//         }
//         &__introduction > * {
//             padding: 0.5rem 1rem;
//         }
//         &__yellow_box {
//             grid-column: 1 / 4;
//             min-width: 400px;
//             padding: 8rem 0;
//             background-color: $primary-red;
//         }
//         &__button {
//             grid-column: 1 / 4;
//             grid-row: 3 / 5;
//             // min-width: 400px;
//             // padding: 2rem 0;
//             border: 2px solid $black;
//             background-color: blue;
//         }
//         &__transparent_box_top,
//         &__transparent_box_bottom {
//             border: 2px solid $black;
//         }
//         &__transparent_box_bottom {
//             grid-column: 4 / 5;
//             grid-row: 3 / 5;
//             background-color: orange;
//         }
//         &__name {
//             font-size: 4rem;
//             font-weight: bold;
//         }
//         &__position {
//             font-size: 1.5rem;
//             font-style: italic;
//             opacity: 0.5;
//         }
//         &__description {
//             line-height: 1.5rem;
//         }
//     }
// }


</style>