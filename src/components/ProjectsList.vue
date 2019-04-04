<template>
<div class="container">
  <p>Let me show you a few choice examples</p>
  <div v-for="project in projects" :key="project.id" class="app-card">
    <h3 class="project-title">{{project.title}}</h3>
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
  name: 'ProjectsList',
  props: {
    msg: String
  },
  data: () => ({
    projects: [
      {
        title: 'Tax Calc',
        id: 11,
        // image: require('@/assets/tax-calc-app.png'),
        image: require('@/assets/taxcalc.png'),
        description: 'Simple calculator to determine sales tax',
        focus: 'Vue frontend framework',
        link: 'http://tax-calc-app.herokuapp.com/'
      },
      {
        title: 'Tree View',
        id: 22,
        // image: require('@/assets/passport-tree.png'),
        image: require('@/assets/datatree.png'),
        description: 'Tree View generator, built using Socket.io and vanilla JS',
        focus: 'Reactive content without a JS Framework',
        link: 'http://tree-4-passport.herokuapp.com/'
      },
      {
        title: 'Pianist Portfolio',
        id: 33,
        // image: require('@/assets/business_card.jpg'),
        // image: require('@/assets/anneportfolio.png'),
        image: require('@/assets/Screenshot_2019-04-04 anne-portfolio-vue.png'),
        description: 'Portfolio site for a collaborative pianist',
        focus: 'Setting up a portfolio site',
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
@import './src/sass/colors';

.container {
  display: flex;
  // width: 80vw;
  flex-direction: column;
  align-items: center;
  margin: 0 5rem;
}

img {
  width: 80%;
  padding: 0.33rem;
  border-radius: 6px;
  background: $light-blue;
  margin: 0 auto;
}

.project-title {
  border-bottom: 0.2rem solid $orange;
  width: 10rem;
  text-align: center;
}

.app-card, a  {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.img-holder {
  // margin: 2rem auto;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
