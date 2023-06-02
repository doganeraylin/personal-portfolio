<script>
export default {
  props: {
    buttonClass: {
      type: String,
      default: 'default-style' 
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
  <div class="container">
    <button :class="buttonClass" @click="handleClick" >
      <div class="button_content">
        <NuxtLink :to="to" v-if="to" class="link_style">{{ buttonText }}</NuxtLink>
        <span v-else>{{ buttonText }}</span>
        <img class="arrow_icon" src="/arrow-icon.png"/>
      </div>
    </button>
  </div>
</template>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.button_content {
  display: flex;
  align-items: center;
  background: transparent;
  cursor: pointer;
  font-size: 1.20rem;
}
.arrow_icon {
  max-width: 1.5rem;
  margin-left: 0.5rem;
  font-weight: 700;
}
.link_style {
  text-decoration: none;
  color: black;
}
.default-style {
  border: none;
}
.primary-style {
  padding: 1rem;
  border: 1px solid black;
}
.primary-style:hover {
  background-color: $primary-blue;
}

@media (min-width: 1080px) {
  .button_content {
    font-size: 2rem;
  }
}
</style>
