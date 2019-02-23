<template>
<div>
  <h1>this is a curtain call.</h1>
  <h3>its name... {{ title }}</h3>
</div>
</template>

<script>
export default {
  name: 'Curtain Call',
  props: {
    msg: String
  },
  data: function() {
    return {
      title: 'fucking seriously?'
    }
  },
  computed: {

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
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
</style>
