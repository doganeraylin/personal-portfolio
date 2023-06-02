<template>
    <footer class="container">
        <div class="container__top_vertical"></div>
        <div class="container__top_horizontal"></div>
        <div class="container__left_yellow"></div>
        <div class="container__left_vertical_thick"></div>
        <div class="container__left_vertical_thin"></div>
        <div class="container__center">
            <div class="container__center_nav">
                <nav >
                    <ul>
                        <li><NuxtLink to="/">home</NuxtLink></li>
                        <li><NuxtLink to="/about">about</NuxtLink></li>
                        <li><NuxtLink to="/projects">projects</NuxtLink></li>
                    </ul>
                </nav>
            </div>
            <div class="container__center_contact">
                <p class="contact_title">Let's connect!</p>
                <!-- <div class="contact_icons">
                    <div class="social_icon">1</div>
                    <div class="social_icon">2</div>
                </div> -->
                <p class="contact_email">doganeraylinn@gmail.com</p>
            </div>
        </div>
        <div class="container__right_vertical_thick"></div>
        <div class="container__right_vertical_thin"></div>
        <div class="container__right_yellow"></div>
        <div class="container__bottom_left"></div>
        <div class="container__copyright">
             <p>Copyright © 2023 Aylin Doğaner</p>
        </div>
        <div class="container__bottom_right"></div>
    </footer>
</template>

<style lang="scss" scoped>
@import "@/styles/variables.scss";
.container {
    display: grid;
    grid-template-columns: repeat(15, 1fr);
    grid-template-rows: repeat(4, 1fr);
    > * {
        border: 2px solid $black;
    }
    &__top_horizontal {
        grid-column: 2 / 16;
    }
    &__left_vertical_thick {
        grid-column: 2 / 4;
        grid-row: 2 / 4;
    }
    &__left_yellow,
    &__right_yellow {
        background-color: $primary-yellow;
    }
    &__bottom_left {
        grid-column: 1 / 4;
    }
    &__copyright {
        grid-column: 4 / 13;
        display: flex;
        justify-content: center;
        font-size: 0.8rem;
    }
    &__copyright p {
        margin: auto 0;
        opacity: 0.5;
    }
    &__right_vertical_thick {
        grid-column: 13 / 15;
        grid-row: 2 / 4;
    }
    &__right_vertical_thin {
        grid-column: 15 / 16;
        grid-row: 2 / 3;  
    } 
    &__bottom_right {
        grid-column: 13 / 16;
    }  
    &__center {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        grid-column: 4 / 13;
        grid-row: 2 / 4;
        padding: 1rem 0 0.5rem;
    }
    &__center_nav ul {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 0.5rem;
        list-style: none;
    }
    &__center_nav a {
        text-decoration: none;
        color: $black;
        padding: 0.5rem 0; 
    }
    &__center_nav li:hover {
        font-weight: bold;
    }
    &__center_contact {
        text-align: center;
        margin: 1rem 0 0;
    }
    &__center_contact p {
        margin: 0.5rem 0;
    }
}

.copyright p {
    font-size: 0.7rem;
}
.contact_title {
    font-weight:700;
}
.contact_email {
    font-size: 0.8rem;
}
.contact_icons {
    display: flex;
    gap: 1rem;
}


@media (min-width: 768px) {
    .container {
        &__center_nav ul {
            flex-direction: row;
            gap: 1.5rem;
            font-size: 1.75rem;
        }
    }
    .contact_title {
        font-size: 1.5rem;
    }
    .contact_email {
        font-size: 1rem;
    }
}
</style>