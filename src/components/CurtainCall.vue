<template>
<div class="container">
  <h1>Hey my name is Jason</h1>
  <h3>I love making websites</h3>

  <div v-for="project in projects" :key="project.id" class="app-card">
    <h4>{{ project.title }}</h4>
    <!-- <img :src="project.image" :alt="project.description"> -->
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
        image: require('@/assets/tax-calc-app.png'),
        description: 'todo',
        focus: 'vue frontend framework'
      },
      {
        title: 'tree view',
        id: 22,
        image: require('@/assets/passport-tree.png'),
        description: '',
        focus: 'reactive content without a JS Framework, vanilla JS only.'
      },
      {
        title: 'pianist portfolio',
        id: 33,
        image: require('@/assets/business_card.jpg'),
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
  align-items: baseline;
  margin-left: 5rem;
}

img {
  height: 20rem;
  padding: 2rem;
  background: #fff;
}
</style>
