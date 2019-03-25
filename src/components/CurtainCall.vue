<template>
<div class="container">
  <h1>this is a curtain call.</h1>
  <h3>its name..</h3>
  <div class="square">
    it went okay, maybe you should checkout this 
  </div>

<!-- 
  <div class="app-card">
    <h4>app one</h4>
    <a rel="stylesheet" href="https://tax-calc-app.herokuapp.com/">
      <div class="img-holder">
        <img src="@/assets/tax-calc-app.png" alt="project one">
      </div>
    </a>
  </div> -->

<div v-for="project in projects" :key="project.id" class="app-card">
    <h4>{{ project.title }}</h4>
    <img :src="project.image" :alt="project.description">
    <a rel="stylesheet" :href="project.link">
      <div class="img-holder">
        <img :src="project.image" v-bind:alt="project.description">
      </div>
    </a>
  </div>

</div>
</template>

<script>
export default {
  name: 'CurtainCall',
  props: {
    msg: String
  },
  data: () => ({
    projects: [
      {
        title: 'tax calc',
        id: 11,
        image: './assets/tax-calc-app.png',
        description: 'todo',
        focus: 'vue frontend framework'
      },
      {
        title: 'tree view',
        id: 22,
        image: '../assets/passport-tree.png',
        description: '',
        focus: 'reactive content without a JS Framework, vanilla JS only.'
      },
      {
        title: 'pianist portfolio',
        id: 33,
        image: '@/assets/passport-tree.png',
        description: 'todo',
        focus: 'setting up a portfolio site for a professsional musician'
      }
    ]
  }),
  computed: {

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  
}
.square {
  height: 23rem;
  width: 23rem;
  background: rgb(00,255,0);
}
</style>
