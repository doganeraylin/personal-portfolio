<script>
export default {
  props: {
    backgroundColor: {
      type: String
    },
    content: {
      type: String,
      default: '' 
    }
  }
};
</script>

<template>
    <div class="container">
        <div class="container__transparent_vertical"></div>
        <div class="container__colored_vertical"></div>
        <div class="container__text">
            <h1>space tourism website</h1>
            <ul>
                <li>and pushing the boundaries of frontend innovation</li>
                <li>and pushing the boundaries of frontend innovation</li>
                <li>and pushing the boundaries of frontend innovation</li>
                <li>and pushing the boundaries of frontend innovation</li>
                <li>and pushing the boundaries of frontend innovation</li>
                <li>and pushing the boundaries of frontend innovation</li>
                <li>and pushing the boundaries of frontend innovation</li>
                <li>and pushing the boundaries of frontend innovation</li>
            </ul>
            <button>see details</button>
        </div>
        <div class="container__screenshot">
            <div></div> 
            <div class="container__links">
                <p><span>live link:</span> www.sthsthsth.com</p>
                <p><span>github link:</span> www.sthsthsth-sthsth.com</p>
            </div>           
        </div>
        <div class="container__bottom_transparent"></div>
    </div>
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
  &__transparent_vertical {
    grid-row: 1 / 3;
  }
  &__colored_vertical {
    grid-column: 1 / 2;
    grid-row: 3 / 5;
    background-color: $black;
  }
  &__text {
    grid-column: 2 / 11;
    grid-row: 1 / 5;
    padding: 1rem 1.5rem;
  }
  &__text ul {
    list-style: none;
    line-height: 2rem;
  }
  &__text > * {
    margin: 0.6rem;
  }
  &__links {
    grid-column: 11 / 16;
    background-color: green;
  }
  &__screenshot {
    grid-column: 11 / 16;
    grid-row: 1 / 4;
  }
  &__bottom_transparent {
    grid-column: 11 / 16;
  }
  button {
    padding: 1rem;
    font-size: 1rem;
  }
}


</style>