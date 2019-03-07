<template>
  <div id="app">
    <div id="nav" class="sidebar">
      <router-link to="/">Home</router-link> 
      <router-link to="/about">Resume</router-link>
      <!-- <router-link to="/about"></router-link> -->
    </div>
    <router-view/>
    <div class="sidebar"></div>
  </div>
</template>

<style lang="scss">
html, body {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: flex;
  justify-content: space-between;
  color: #2c3e50;
}
.sidebar{
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 30px;
  background: orange; 
}
#nav {
  // display: none;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 30px;
  background: orange;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
