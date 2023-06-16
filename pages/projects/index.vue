<template>
    <Navbar/>
    <Journey/>
    <TechStackLayout/>
    <TechStack/>
    <ProjectLayout :projects="projects"/>
    <Footer/>
</template>

<script>
import Journey from "@/components/Projects/Journey.vue"
import TechStackLayout from "@/components/Projects/TechStackLayout.vue"
import TechStack from "@/components/Projects/TechStack.vue"
import ProjectLayout from "~/components/Projects/ProjectLayout.vue"


export default {
    data() {
        return {
            projects: []
        }
    },
    components: {
        Journey, 
        TechStackLayout,
        TechStack,
        ProjectLayout
    },
    async mounted() {
        try {
            const response = await fetch('https://personal-portfolio-api-cyan.vercel.app/projects');
        if (response.ok) {
            this.projects = await response.json();
        } else {
            console.error('Failed to fetch projects:', response.status);
        }
        } catch (error) {
            console.error('Error:', error);
        }
    }   
}
</script>


<style lang="scss" scoped>
@import "@/styles/variables.scss";
</style>