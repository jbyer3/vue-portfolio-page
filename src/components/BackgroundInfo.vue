<template>
<div class="container">
  <h1>Hey my name is Jason, and
  I love making websites</h1>
  <h2>let me tell you a little something <span>about myself</span></h2>
</div>
</template>

<script>
export default {
  name: 'BackgroundInfo',
  props: {
    msg: String
  },
  data: () => ({
    
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
  flex-direction: column;
  align-items: baseline;
  margin-left: 5rem;
}

img {
  width: 50rem;
  padding: 0.24rem;
  border-radius: 6px;
  // background: lighten($light-blue, 65%);
  background: $light-blue;
}

</style>
