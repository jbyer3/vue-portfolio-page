<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <CurtainCall/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import CurtainCall from '@/components/CurtainCall.vue'

export default {
  name: 'home',
  components: {
    HelloWorld,
    CurtainCall
  }
}
</script>
