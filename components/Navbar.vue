<script>
export default {
  data() {
    return {
      isMenuOpen: false
    };
  },
  methods: {
    toggleMenu() {
      console.log("clicked")
      this.isMenuOpen = !this.isMenuOpen;
    }
  }
};
</script>

<template>
  <header class="container">
    <input type="checkbox" id="nav_toggle" :class="{ 'expanded': isMenuOpen }" class="nav_toggle" @click="toggleMenu">
    <nav>
      <ul>
        <li><NuxtLink to="/">home</NuxtLink></li>
        <li><NuxtLink to="/about">about</NuxtLink></li>
        <li><NuxtLink to="/projects">projects</NuxtLink></li>
      </ul>
    </nav>
    <label for="nav_toggle" class="nav_toggle_label">
      <span></span>
    </label>
  </header>
</template>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

.container {
  text-align: center;
  width: 100%;
  border: 1px solid black;
  height: 80px;
}
.nav_toggle {
  position: absolute !important;
  // top: -9999px !important;
  left: -9999px !important;
}

.nav_toggle_label {
  position: absolute;
  top: 2rem;
  left: 0;
  margin-left: 1rem;
  display: flex;
  align-items: center;
}

.nav_toggle_label span,
.nav_toggle_label span::before,
.nav_toggle_label span::after {
  display: block; 
  background-color: black ;
  height: 5px;
  width: 2em;
  border-radius: 2px;
  position: relative;
  cursor: pointer;
}

.nav_toggle_label span::before,
.nav_toggle_label span::after {
  content: '';
  position: absolute;
}

.nav_toggle_label span::before {
  bottom: 7px;
}

.nav_toggle_label span::after {
  top: 7px;
}

nav {
  text-align: left;
  width: 100%;
  background-color: $primary-gray;
  transform: scale(1, 0);
  transform-origin: top;
  transition: transform 400ms ease-in-out;
}

nav ul {
  margin: 3.5rem 0;
  padding: 1.5rem 0;
  list-style: none;
  border: 1px solid $black;
}

nav li {
  margin-bottom: 1rem;
  margin-left: 1rem;
}

nav a {
  color: black;
  text-decoration: none;
  font-size: 1.2rem;
  opacity: 0;
  transition: opacity 150ms ease-in-out;
}

nav a:hover {
  font-weight: 700;
}

.nav_toggle:checked ~ nav {
  transform: scale(1,1);
}

.nav_toggle:checked ~ nav a {
  opacity: 1;
  transition: opacity 250ms ease-in-out 250ms;
}

@media screen and (min-width: 768px) {
  .nav_toggle_label {
    display: none;
  }
  nav {
    text-align: left;
    transition: none;
    display: flex;
    transform: scale(1,1);
    padding: 1.2rem;
  }
  nav ul {
    display: flex;
    align-items: center;
    justify-content: space-around;
    margin: 0;
    padding: 0;
    border: none;
  }
  nav li {
    margin-bottom: 0;
  }
  nav a {
    opacity: 1;
    margin: 0 1rem;
    font-size: 1.75rem;
  }
}


</style>