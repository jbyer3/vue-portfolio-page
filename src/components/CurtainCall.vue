<template>
<div class="container">
  <h1>this is a curtain call.</h1>
  <h3>its name..</h3>
  <div class="square">
    it went okay
  </div>
</div>
</template>

<script>
export default {
  name: 'CurtainCall',
  props: {
    msg: String
  },
  data: function() {
    return {
      title: 'seriously?'
    }
  },
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
  align-items: center;
  
}
.square {
  height: 23rem;
  width: 23rem;
  background: rgb(00,255,0);
}
</style>
