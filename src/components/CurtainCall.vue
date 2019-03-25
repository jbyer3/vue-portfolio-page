<template>
<div class="container">
  <h1>Hey my name is Jason, and
  I love making websites</h1>

  <p>let me show you a few choice examples</p>

  <div v-for="project in projects" :key="project.id" class="app-card">
    
    <!-- <img :src="project.image" :alt="project.description"> -->
      <h3>{{ project.title }}</h3>
      <div class="img-holder">
        <a :href="project.link">
          <img :src="project.image" v-bind:alt="project.description">
        </a>
        <p><span class="img-cap-title">description: </span>{{project.description}}</p>
        <p><span class="img-cap-title">focus: </span>{{project.focus}}</p>
      </div>
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
        description: 'a simple calculator to determine sales tax',
        focus: 'vue frontend framework',
        link: 'http://tax-calc-app.herokuapp.com/'
      },
      {
        title: 'tree view',
        id: 22,
        image: require('@/assets/passport-tree.png'),
        description: 'a tree view generator, built using websockets and vanilla javascript',
        focus: 'reactive content without a JS Framework, vanilla JS only.',
        link: 'http://tree-4-passport.herokuapp.com/'
      },
      {
        title: 'pianist portfolio',
        id: 33,
        image: require('@/assets/business_card.jpg'),
        description: 'a portfolio site for my girlfriends business as a collaborative pianist',
        focus: 'setting up a portfolio site for a professsional musician',
        link: 'https://www.pengillyplayspiano.com/'
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
  width: 50rem;
  padding: 2rem;
  background: #fff;
}

.img-cap-title {
  // color: darken(22%)
}
</style>
