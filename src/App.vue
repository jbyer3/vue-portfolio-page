<template>
  <div id="app">
    <div id="nav">
      <div class="nav-left">
        <router-link to="/">Home</router-link> 
        <router-link to="/about">About</router-link>
      </div>
      <div class="nav-right">
        Jason <span class="last-name">Byer</span>
      </div>
    </div>
    <router-view/>
    <footer>
      <div class="footer-left">
        <span>Say hello to me</span>
      </div>
      <div class="footer-right">
        <div v-for="link in externLinks" :key="link.id">
          <a :href="link.link">
            <span>{{link.site}}</span>
            <img :src="link.image" :alt="link.alt">
          </a>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  data: () => ({
    externLinks: [
      {
        site: 'github',
        image: require('@/assets/GitHub-Mark-Light-32px.png'),
        alt: 'link to github page',
        link: 'https://github.com/jbyer3',
        id: 1
      },
      {
        site: 'linkedin',
        image: require('@/assets/In-White-34px-TM.png'),
        alt: 'link to linkedin page',
        link: 'https://www.linkedin.com/in/jason-byer-a88493141/',
        id: 2
      }
    ]
    
  })
}
</script>


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
  width: 100%;
}

#nav, footer {
  // width: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  padding: 30px;
  background: $orange;
  color: $offwhite;
  border-bottom: $light-blue 0.4em solid;
  letter-spacing: 2px;
  a {
    font-weight: bold;
    // color: $black;
    color: $offwhite;
    margin-right: 1rem;
    &.router-link-exact-active {
      // color: $offwhite;
      color: lighten($light-blue, 20%);
      // color: $light-blue;
    }
  }
}

.nav-right, .footer-right {
  // padding: 0;
  // margin: 0;
  color: $offwhite;
  // color: $black;
  font-weight: 700;
  font-size: 1.4rem;
  display: flex;
  justify-content: flex-end;
}

.last-name {
  // color: darken($orange, 33%);
  color: lighten($light-blue, 20%);
  // color: $light-blue;
  margin-left: 0.3em;
}

.footer-left {
  font-size: 1.4rem;
}
</style>
