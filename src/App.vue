<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> 
      <router-link to="/resume">Resume</router-link>
      <!-- <router-link to="/about"></router-link> -->
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
@import './src/sass/colors';

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
  flex-direction: column;
  color: $black;
  background: $offwhite;
  min-height: 300px;

}

#nav {
  // display: none;
  display: flex;
  // flex-direction: column;
  align-items: flex-start;
  padding: 30px;
  background: $orange;
  a {
    font-weight: bold;
    color: $black;
    margin-right: 2rem;
    &.router-link-exact-active {
      // color: lighten($ofwhite, 15%);
      color: $offwhite;
    }
  }
}
</style>
