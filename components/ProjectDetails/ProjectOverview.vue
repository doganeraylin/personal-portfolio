<template>
    <div class="container">
        <div class="container__red"></div>
        <div class="container__details_title">
            <h2>Project Overview</h2>
        </div>
        <div class="container__black"></div>
        <div class="container__details_description">
            <p>{{project.overview}}</p>
        </div>      
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
        grid-column: 1 / 4;
    }
    &__red {
        background-color: $primary-red;
    }
    &__black {
        background-color: $black;
    }
}
</style>