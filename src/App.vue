<template>
  <div id="app">
    <div id="nav">
      <div class="nav-left">
        <router-link to="/">Home</router-link> 
        <router-link to="/about">About</router-link>
      </div>
      <div class="nav-right">
        Jason Byer
      </div>
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
  width: 100vw;
}

#nav {
  // width: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  padding: 30px;
  background: $orange;
  border-bottom: $light-blue 0.4em solid;
  letter-spacing: 2px;
  a {
    font-weight: bold;
    color: $black;
    margin-right: 1rem;
    &.router-link-exact-active {
      color: $offwhite;
    }
  }
}

.nav-right {
  // padding: 0;
  // margin: 0;
  color: $offwhite;
  font-weight: 700;
  font-size: 1.4rem;
  display: flex;
  justify-content: flex-end;
}
</style>
