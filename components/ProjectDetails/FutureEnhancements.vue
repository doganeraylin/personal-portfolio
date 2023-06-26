<template>
    <div class="details_container">
        <div class="details_container__yellow"></div>
        <div class="details_container__title">
            <h2>Future Enhancements</h2>
        </div>
        <div class="details_container__red"></div>
        <div class="details_container__description">
          <ul v-for="futureEnhancement in project.futureEnhancements" :key="futureEnhancement.id" class="details_container__list">
            <li>{{futureEnhancement.text}}</li>
          </ul>
        </div>   
        <div class="details_container__horizontal_transparent"></div>   
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
.details_container {
  &__horizontal_transparent {
      grid-column: 1 / 6;
      padding: 1rem;
  }
}
</style>