<template>
  <div class="container">
    <div class="carousel">
      <div class="slides" :style="`transform: translateX(-${slideIndex * 100}%)`">
        <div v-for="(image, index) in project.screenshots" :key="index" class="slide">
          <div class="screenshot_container">
            <img class="screenshot_container__img" :src="image.image" :alt="`Slide ${index + 1}`">
          </div>
        </div>
      </div>
    </div>
    <div class="dots">
      <button v-for="(image, index) in project.screenshots" :key="index" @click="goToSlide(index)" :class="{ active: index === slideIndex }"></button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    project: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      slideIndex: 0,
    };
  },
  methods: {
    goToSlide(index) {
      this.slideIndex = index;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.screenshot_container {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  margin: 0 auto;
  &__img {
     grid-column: 2 / 5;
    max-width: 100%;
    margin: 1rem 0;
    border: 3px solid $black;
  }
}
.carousel {
 
  position: relative;
  overflow: hidden;
  display: flex;
  align-items: center;
  max-height: 820px;
  padding: 0;
  margin: 0;
}
.slides {
  display: flex;
  transition: transform 0.3s ease-in-out;
}
.slide {
  flex-shrink: 0;
  width: 100%;
  overflow-y: hidden;
}
.right {
  font-size: 10rem;
  border: 5px solid red;
}
.dots {
  display: flex;
  justify-content: center;
  margin: 1rem 0;
}
.dots button {
  width: 1rem;
  height: 1rem;
  border: none;
  background: #ccc;
  margin: 0 4px;
  padding: 0;
}
.dots button.active {
  background-color: $primary-red;
}

@media (min-width: 1440px) {
  .dots button {
  
  }
}
</style>
