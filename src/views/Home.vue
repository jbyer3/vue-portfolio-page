<template>
  <div class="home">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- content, like stories goes vertically. parallax scrolling images -->
    <!-- hover drawers on left and right for projects and contact respectively -->
    <LeftDrawer class="sidebar" />
    <CurtainCall class="main" />
    <RightDrawer class="sidebar" />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import LeftDrawer from '@/components/LeftDrawer.vue'
import CurtainCall from '@/components/CurtainCall.vue'
import RightDrawer from '@/components/RightDrawer.vue'

export default {
  name: 'home',
  components: {
    // HelloWorld,
    LeftDrawer,
    CurtainCall,
    RightDrawer
  }
}
</script>

<style lang="scss" scoped>
.home {
  display: flex;
  height: 100vh;
  .sidebar {
    background: red;
    height: 100%;
    flex-grow: 1;
  }
  .main {
    background: green;
    height: 100%;
    flex-grow: 3;
  }
}
</style>

