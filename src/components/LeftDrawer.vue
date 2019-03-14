<template>
<div class="container">
  <div class="app-card">
    <h4>app one</h4>
    <a rel="stylesheet" href="https://tax-calc-app.herokuapp.com/">
      <div class="img-holder">
        <img src="@/assets/tax-calc-app.png" alt="project one">
      </div>
    </a>
  </div>
</div>
</template>

<script>
export default {
  name: 'LeftDrawer',
  props: {
    msg: String
  },
  data: () => ({
    projects: [
      {
        title: 'tax calc',
        id: 11,
        image: '@/assets/tax-calc-app.png',
        description: 'todo',
        focus: 'vue frontend framework'
      },
      {
        title: 'tree view',
        id: 22,
        image: '@/assets/passport-tree.png',
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
  })
  ,
  computed: {

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.app-card {
  // height: 2rem;
  width: 23rem;
  background: lightcoral;
  padding: 2rem;
  margin: 4rem 0;
  // width: 100%;
  img {
    width: 100%;
  }
}

.container {
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  align-items: center;
}

</style>
