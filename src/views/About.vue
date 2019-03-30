<template>
  <div class="about">
    <ConstructionPage/>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import ConstructionPage from '@/components/ConstructionPage.vue';
export default {
  name: 'home',
  components: {
    // HelloWorld,
    ConstructionPage
  },
  data: () => ({
    
  })
}
</script>