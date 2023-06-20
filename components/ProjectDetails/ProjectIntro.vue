<template>
    <div class="container">
        <div class="container__black"></div>
        <div class="container__title">
            <h1>{{project.title}}</h1>
        </div>
        <div class="container__red"></div>
        <div class="container__left_transparent"></div>
        <div v-for="link in project.links" :key="link.id" class="container__links">
            <ul>
                <li v-if="project.links[0].liveProject"> 
                    <span>live project: </span>
                    <NuxtLink  
                    class="container__single_link" 
                    :to="link.liveProject" 
                    target="_blank">{{link.liveProject}}
                    </NuxtLink>
                </li>
                <li><span>github link: </span><NuxtLink class="container__single_link" :to="link.github" target="_blanks">{{link.github}}</NuxtLink></li>
            </ul>
        </div>
        <div class="container__right_transparent"></div>
    </div>
</template>

<script>
export default {
  props: {
    project: {
      required: true,
    },
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";
.container {
    display: grid;
    grid-template-columns: repeat(9, 1fr);
    text-align: center;
    > * {
        border: 1px solid black;
    }

    &__black {
        background-color: $black;
    }
    &__title,
    &__links {
        grid-column: 2 / 9;
    }
    &__title {
        padding: 1.75rem;
        font-size: 1.5rem;
    }
    &__links {
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 1.5rem;
        line-height: 1.75rem;
        font-style: italic;
    }
    span {
        font-style: normal;
        margin-right: 1rem;
    }
    &__red {
        background-color: $primary-red;
    }
    &__links ul {
        list-style: none;
    }
    &__links li {
        font-weight: bold;
    }
    &__single_link {
        background-color: $primary-yellow;
        color: $black;
    }
}

@media (min-width: 992px) {
    .container {
        &__title {
            padding: 2rem;
            text-transform: uppercase;
        }
    }
}
</style>