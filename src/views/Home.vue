<template>
  <div class="home">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <BackgroundInfo/>
    <ProjectsList/>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import ProjectsList from '@/components/ProjectsList.vue'
import BackgroundInfo from '@/components/BackgroundInfo.vue'

export default {
  name: 'home',
  components: {
    // HelloWorld,
    ProjectsList,
    BackgroundInfo,
  },
  data: () => ({
    
  })
}
</script>