<template>
  <div class="home">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- content, like stories goes vertically. parallax scrolling images -->
    <!-- hover drawers on left and right for projects and contact respectively -->
    <CurtainCall class="main" />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import CurtainCall from '@/components/CurtainCall.vue'

export default {
  name: 'home',
  components: {
    // HelloWorld,
    CurtainCall,
  },
  data: () => ({
    
  })
}
</script>

<style lang="scss">
@import './src/sass/colors';

.home {
  color: $black;
}
</style>
