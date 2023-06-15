<template>
    <div class="container">
        <div class="container__yellow"></div>
        <div class="container__details_title">
            <h2>Future Enhancements</h2>
        </div>
        <div class="container__red"></div>
        <div class="container__transparent"></div>
        <div class="container__details_description">
            <p>{{project.futureEnhancements}}</p>
        </div>   
        <div class="container__horizontal_transparent"></div>   
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
    text-align: center;
    > * {
        border: 2px solid $black;
    }
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    &__details_description {
        grid-column: 1 / 6;
    }
    &__yellow {
        background-color: $primary-yellow;
    }
    &__red {
        background-color: $primary-red;
    }
    &__horizontal_transparent {
        grid-column: 1 / 6;
        padding: 1rem;
    }
}
</style>