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
            <h1 class="container__title">space tourism website</h1>
            <ul>
                <li>and pushing the boundaries of frontend innovation of frontend innovation</li>
                <li>and pushing the boundaries of frontend innovation</li>
                <li>and pushing the boundaries of frontend innovation</li>
                <li>and pushing the boundaries of frontend innovation</li>
                <li>and pushing the boundaries of frontend innovation</li>
                <li>and pushing the boundaries of frontend innovation</li>
                <li>and pushing the boundaries of frontend innovation</li>
                <li>and pushing the boundaries of frontend innovation</li>
            </ul>
            <div class="container__button">
              <Button 
                buttonText="see details" 
                buttonClass="primary-style"
              />
            </div>
        </div>
        <div class="container__preview">
            <div class="container__screenshot">img</div> 
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
  grid-template-columns: repeat(8, 1fr);
    grid-template-rows: repeat(4, 1fr);
  > * {
    border: 2px solid $black;
  }
 
  &__text {
    grid-column: 1 / 9;
    grid-row: 1 / 4;
    padding: 1.5rem 1rem;
  }
  &__text ul {
    list-style: none;
    line-height: 2rem;
  }
  &__text > * {
    margin: 0.6rem;
  }
  .button:hover {
    background-color: $primary-blue;
  }
  &__transparent_vertical,
  &__colored_vertical,
  &__bottom_transparent,
  &__screenshot {
    display: none;
  }
  &__preview {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    grid-column: 1 / 9;
  }
}

@media (min-width: 992px) {
  
.container {
    &__transparent_vertical,
    &__colored_vertical,
    &__bottom_transparent,
    &__screenshot {
      display: block;
    }
    &__transparent_vertical {
      grid-row: 1 / 3;
    }
    &__colored_vertical {
      grid-row: 3 / 5;
      background-color: $primary-red;
    }
    &__text {
      grid-column: 2 / 6;
      grid-row: 1 / 5;
      padding: 1.5rem 1rem;
    }
    &__preview,
    &__bottom_transparent {
      grid-column: 6 / 9;
    }
    &__preview {
      grid-row: 1 / 4;
      background: green;
    }
    &__bottom_transparent {
      grid-row: 4 / 5;
    }
    &__title {
      text-transform: uppercase;
    } 
  }

}


</style>