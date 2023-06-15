<template>
   <div class="container">
       <div v-for="image in project.screenshots.desktop" :key="image.id" class="container_desktop">
           <img class="container_desktop__screenshot" :src="image.image">
        </div>
        <div v-for="image in project.screenshots.mobile" :key="image.id" class="container_mobile">
           <img class="container_mobile__screenshot" :src="image.image">
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
    display: flex;
    align-items: center;
    overflow: hidden;

}

.container_desktop,
.container_mobile {
    display: flex;

    &__screenshot {
        max-width: 200px;
        margin: 1rem;
    }
}
.container_mobile {
    &__img {
        padding: 10rem 7rem;
        border: 1px solid black;
        margin: 1rem 0;
    }
}


</style>