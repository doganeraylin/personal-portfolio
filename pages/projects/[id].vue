<template>
  <div>
    <Navbar/>
    <ProjectIntro :project="project" />
    <ProjectOverview :project="project"/>
    <KeyFeatures :project="project"/>
    <FutureEnhancements :project="project"/>
    <Screenshots :project="project"/>
  </div>
</template>

<script setup>
    import ProjectIntro from "@/components/ProjectDetails/ProjectIntro.vue"
    import ProjectVideo from "@/components/ProjectDetails/ProjectVideo.vue"
    import ProjectOverview from "@/components/ProjectDetails/ProjectOverview.vue"
    import KeyFeatures from "@/components/ProjectDetails/KeyFeatures.vue"
    import FutureEnhancements from "@/components/ProjectDetails/FutureEnhancements.vue"
    import Screenshots from "@/components/ProjectDetails/Screenshots.vue"

    const { id } = useRoute().params
    const uri = 'https://personal-portfolio-api-cyan.vercel.app/projects/' + id

    const { data: project } = await useFetch(uri, { key: id })

    if (!project.value) {
    throw createError({ statusCode: 404, statusMessage: 'project not found' })
    }
</script>

