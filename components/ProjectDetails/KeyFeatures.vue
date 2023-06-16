<template>
    <div class="details_container">
        <div class="details_container__yellow"></div>
        <div class="details_container__title">
            <h2>Key Features</h2>
        </div>
        <div class="details_container__transparent"></div>
        <div  class="details_container__description">
            <ul class="details_container__details_list" v-for="text in project.keyFeatures" :key="text.id">
                <li>{{text.text}}</li>
            </ul>
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
.details_container {
    &__horizontal_transparent {
        padding: 1rem;
    }
    &__details_list li {
        padding: 1rem;
        line-height: 1.75rem;
        list-style-type: square;
    }
}
</style>