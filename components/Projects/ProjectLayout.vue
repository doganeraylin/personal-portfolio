<template>
    <div class="container">
        <div class="container__transparent_vertical"></div>
          <div v-for="project in projects" :key="project.title" class="container__content">
            <div class="container__single_content">
              <h1 class="container__title">{{ project.title }}</h1>
              <p class="container__overview">{{ project.overview }}</p>
              <div class="container__button">
                <Button 
                  buttonText="see details" 
                  :to="`/projects/${project.id}`"
                />
            </div>
          </div>
        </div>
    </div>
</template>

<script>
export default {
  props: {
    backgroundColor: {
      type: String
    },
    projects: {
      type: Array,
      required: true
    }
  }
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.container {
      display: grid;
  > * {
       border: 3px solid $black;
  }

  &__transparent_vertical {
    padding: 3rem;
  }
  
  &__single_content {
    padding: 1rem;
    margin: 2rem 0;
  }
  &__single_content > * {
    max-width: 70%;
    margin: 1rem auto;
  }
  &__title {
      background: $primary-yellow;
      color: $black;
      padding: 1rem;
      border: 2px solid black;
  }
  &__overview {
    line-height: 1.7rem;
    border: 2px solid $black;
    padding: 1rem;
    background-color: $primary-blue;
    color: $primary-gray;
  }
  &__title,
  &__overview {
    padding: 1.5rem 2.2rem;
  }
}

@media (min-width: 1024px) {
  .container {
    &__single_content > * {
      max-width: 70%;
      margin: 1rem auto;

    }
    &__title {
      font-size: 3rem;
    }
    &__overview {
      font-size: 1.75rem;
      line-height: 2.5rem;
    }
  }
}
</style>
