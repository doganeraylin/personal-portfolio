<template>
    <div class="details_container">
        <div class="details_container__red"></div>
        <div class="details_container__title">
            <h2>Project Overview</h2>
        </div>
        <div class="details_container__black"></div>
        <div class="details_container__description">
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
