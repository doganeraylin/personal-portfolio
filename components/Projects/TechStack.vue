

<template>
<div class="wrapper">
  <div class="container" ref="containerRef">
    <div class="container__transparent"></div>
    <div class="tech_stack_container">
      <div class="scroll-wrapper" ref="scrollWrapperRef">
        <div class="tech_stack" v-for="tech in techStack" :key="tech.id">
          <img :src="tech.img">
          <p>{{ tech.title }}</p>
        </div>
      </div>
    </div>
  </div>
</div>

</template>

<script>
import gsap from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';

export default {
  data() {
    return {
      techStack: [],
    };
  },
  mounted() {
    this.loadContent();
    console.log("this load content");
  },

  updated() {
    gsap.registerPlugin(ScrollTrigger);
    if (this.techStack.length > 0) {
      this.initializeScrollAnimation();
    }
  },
  
  methods: {
    loadContent() {
      return new Promise((resolve, reject) => {
        fetch('https://personal-portfolio-api-cyan.vercel.app/techStack')
          .then(response => response.json())
          .then(data => {
            this.techStack = data;
            resolve();
        })
        .catch(error => {
          console.error(error);
          reject(error);
        });
      });
    },

    initializeScrollAnimation() {
      const container = this.$refs.containerRef;
      const scrollWrapper = this.$refs.scrollWrapperRef;
      const techStackItems = Array.from(scrollWrapper.children);
      gsap.to(techStackItems, {
      xPercent: -100* (techStackItems.length - 1),
      ease: "none",
      scrollTrigger: {
        trigger: this.$refs.containerRef,
        pin: true,
        scrub: 1,
        end:"+3000"
      }
    })
    }
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";
  .wrapper {
    overflow-x: hidden;
  }
  .container {
    max-width: 1500px;
    gap: 1rem;
    min-height: 250px;
  }
  .scroll-wrapper {
    display: flex;
  }
  .tech_stack {
    border: 1px solid $black;
    text-align: center;
    padding: 0.5rem;
    margin: 4rem 0.5rem 0;
    img {
      max-width: 120px;
    }
    p {
      font-size: 1rem;
      opacity: 0.5;
      margin: 1rem 0 0;
    }
  }

  // @media (min-width: 1024px) {
  //   .tech_stack {
      
  //   }
  // }
</style>