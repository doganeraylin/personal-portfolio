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
  <header>
    <input type="checkbox" id="nav-toggle" :class="{ 'expanded': isMenuOpen }" class="nav-toggle" @click="toggleMenu">
    <nav >
      <ul>
        <li><NuxtLink to="/">home</NuxtLink></li>
        <li><NuxtLink to="/about">about</NuxtLink></li>
        <li><NuxtLink to="/projects">projects</NuxtLink></li>
      </ul>
    </nav>
    <label for="nav-toggle" class="nav-toggle-label">
      <span></span>
    </label>
  </header>
</template>

<style lang="scss" scoped>

header {
  text-align: center;
  // z-index: 999;
  width: 100%;
  border: 1px solid black;
  height: 80px;
}
.nav-toggle {
  position: absolute !important;
  // top: -9999px !important;
  left: -9999px !important;
}

.nav-toggle-label {
  position: absolute;
  top: 2rem;
  left: 0;
  margin-left: 1rem;
  display: flex;
  align-items: center;
}

.nav-toggle-label span,
.nav-toggle-label span::before,
.nav-toggle-label span::after {
  display: block; 
  background-color: black ;
  height: 5px;
  width: 2em;
  border-radius: 2px;
  position: relative;
  cursor: pointer;
}

.nav-toggle-label span::before,
.nav-toggle-label span::after {
  content: '';
  position: absolute;
}

.nav-toggle-label span::before {
  bottom: 7px;
}

.nav-toggle-label span::after {
  top: 7px;
}

nav {
  text-align: left;
  width: 100%;
  transform: scale(1, 0);
  transform-origin: top;
  transition: transform 400ms ease-in-out;
}

nav ul {
  margin: 3.5rem 0;
  padding: 0;
  list-style: none;
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

// nav a:hover {
//   color:#000;
// }

.nav-toggle:checked ~ nav {
  transform: scale(1,1);
}

.nav-toggle:checked ~ nav a {
  opacity: 1;
  transition: opacity 250ms ease-in-out 250ms;
}



@media screen and (min-width: 768px) {
  .nav-toggle-label {
    display: none;
  }

  nav {
    text-align: left;
    transition: none;
    transform: scale(1,1);
    display: flex;
    justify-content: flex-start;
    align-items: center;
  }
  
  nav ul {
    display: flex;
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