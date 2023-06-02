<template>
    <div class="container">
        <Navbar/>
        <HelloSection/>
        <StatementOne/>
        <StatementTwo/>
        <StatementThree/>
        <Footer/>
    </div>
</template>

<script>
import HelloSection from "@/components/About/HelloSection.vue"
import StatementOne from "@/components/About/StatementOne.vue"
import StatementTwo from "@/components/About/StatementTwo.vue"
import StatementThree from "@/components/About/StatementThree.vue"

export default {
    components : {
        HelloSection,
        StatementOne,
        StatementTwo,
        StatementThree,
    }
}
</script>

