<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> 
      <router-link to="/about">About</router-link>
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
  display: flex;
  align-items: flex-start;
  padding: 30px;
  background: $orange;
  border-bottom: $light-blue 0.4em solid;
  a {
    font-weight: bold;
    color: $black;
    margin-right: 1rem;
    &.router-link-exact-active {
      color: $offwhite;
    }
  }
}
</style>
