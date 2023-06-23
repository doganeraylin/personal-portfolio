<script>
export default {
  props: {
    buttonClass: {
      type: String,
      default: 'button_content' 
    },
    buttonText: {
      type: String,
      default: 'button' 
    },
    clickHandler: {
      type: String,
    },
    to: {
      type: [String, Object],
      default: null
    },
  },
}
</script>

<template>
  <NuxtLink :to="to" v-if="to" class="link_style">
    <div class="container">
      <div class="button_container">
        <button :class="buttonClass">
          <div class="button_content">
            {{ buttonText }}
            <img class="arrow_icon" src="/arrow-icon.png" />
          </div>
        </button>
      </div>
    </div>
  </NuxtLink>

  <span v-else>
    <div class="container">
      <div class="button_container">
        <button :class="buttonClass">
          <div class="button_content">
            {{ buttonText }}
            <img class="arrow_icon" src="/arrow-icon.png" />
          </div>
        </button>
      </div>
    </div>
  </span>
</template>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.button_content {
  background: transparent;
  cursor: pointer;
  text-align: left;
  padding: 1rem 0.5rem;
}
.button_content:hover {
  background-color: $primary-red;
}
.arrow_icon {
  max-width: 1.2rem;
  font-weight: 700;
  margin-left: 0.5rem;
}
.button_secondary {
  font-size: 1rem;
  border: 1px solid $black;
  background: transparent;
}
.button_secondary:hover {
  background-color: $primary-blue;
}
.link_style {
  text-decoration: none;
  color: $black;
}

@media (min-width: 768px) {
  .button_content {
    font-size: 2rem;
  }
}
</style>
