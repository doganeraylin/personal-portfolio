<template>
    <div class="container">
        <Navbar/>
        <HelloSection/>
        <StatementOne/>
        <StatementTwo/>
        <StatementThree/>
        <Journey/>
        <TechStackLayout/>
        <TechStack/>
        <ProjectLayout1/>
        <ProjectLayout2/>
        <ProjectLayout1/>
        <ProjectLayout2/>
        <Footer/>
    </div>
</template>

<script>
import HelloSection from "@/components/About/HelloSection.vue"
import StatementOne from "@/components/About/StatementOne.vue"
import StatementTwo from "@/components/About/StatementTwo.vue"
import StatementThree from "@/components/About/StatementThree.vue"
import Journey from "@/components/About/Journey.vue"
import TechStackLayout from "@/components/About/TechStackLayout.vue"
import TechStack from "@/components/About/TechStack.vue"
import ProjectLayout1 from "@/components/About/ProjectLayout1.vue"
import ProjectLayout2 from "@/components/About/ProjectLayout2.vue"
export default {
    components : {
        HelloSection,
        StatementOne,
        StatementTwo,
        StatementThree,
        Journey,
        TechStackLayout,
        TechStack,
        ProjectLayout1,
        ProjectLayout2
    }
}

</script>

