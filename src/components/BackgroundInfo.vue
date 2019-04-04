<template>

  <div class="container">

    <div class="header-content">
      <h1 class="bold-statement">My name is Jason</h1>
      <!-- <div class="break-and">-and I love making websites-</div>
      <h2>I love making websites</h2> -->

      <p id="intro-statement">let me tell you a little something <span class="intro-bolder">about myself</span>!</p>
    </div>

    <p class="bio-statement">Have you ever heard of a flashbulb memory? My flashbulb memory was sitting in One World Brewing in Asheville, talking to my sister's boyfriend, Seth. He saw that I was really struggling with depression in the current moment and wanted to offer a lifeline to me. <span class="exclamation-text">"You should look at learning how to code!"</span> I had initially shrugged him off saying that it wasn't anything crazy. "I don't have a brain for computers", I said, not having any idea what that actually entailed. I had not even given his words a second thought until I returned home after that weekend. After only a few days of experimentation with some online resources I discovered that this was exactly what I was meant to do with my life.</p>

    <p class="bio-statement">The next year I spent doing as much as I possibly could to get as much experience as possible. It would actually turn out to be the most transformative year of my life thus far. Working and spending time with tons of different developers taught me a lot about how to write code, and even more about myself. I learned how to channel my existing talents and newfound skills into a workflow that I finally felt proud of. One thought easily brought to mind is, "Oh dear, if only I had started earlier! I would be so much better!" I dismiss that as quickly as I can. Some people will go through their whole lives and never find a passion that they can honestly feel gives them purpose, and I love knowing that there is always a new tangle to unravel just ahead of me. </p>
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
  // margin: 0 5rem;
}

.header-content {
  width: 95%;
  text-align: center;
}

img {
  width: 50rem;
  padding: 0.24rem;
  border-radius: 6px;
  // background: lighten($light-blue, 65%);
  background: $light-blue;
}

.bold-statement {
  margin: 2.6rem auto 3.2rem;
}

#intro-statement {
  font-size: 1.5rem;
  // margin-left: 9%;
  .intro-bolder {
  font-weight: 600;
  }
}

.bio-statement {
  text-indent: 3rem;
  width: 66%;
  margin-left: 5rem;
  line-height: 1.5;
}

.exclamation-text {
  margin: 10px;
  display: block;
  text-indent: 0;
  font-style: italic;
  font-weight: 600;
}

.break-and {
  padding: 0;
  margin: 0;
}
</style>
