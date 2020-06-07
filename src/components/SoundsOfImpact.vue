<template>
  <div>
    <h1>{{ msg }}</h1>
    <ul id="birds" >
      <li><img class="logo" alt="Temporary Logo" :src="bird1"></li>
      <li><img class="logo" alt="Temporary Logo" src="https://nas-national-prod.s3.amazonaws.com/styles/hero_image/s3/web_groombaltimoreoriole-and-a-male-red-breasted-grosbeak.jpg?itok=mGKiNpgF"></li>
      <li><img class="logo" alt="Temporary Logo" src="https://nas-national-prod.s3.amazonaws.com/styles/hero_image/s3/web_groombaltimoreoriole-and-a-male-red-breasted-grosbeak.jpg?itok=mGKiNpgF"></li>
      <li><img class="logo" alt="Temporary Logo" src="https://nas-national-prod.s3.amazonaws.com/styles/hero_image/s3/web_groombaltimoreoriole-and-a-male-red-breasted-grosbeak.jpg?itok=mGKiNpgF"></li>
      <li><img class="logo" alt="Temporary Logo" src="https://nas-national-prod.s3.amazonaws.com/styles/hero_image/s3/web_groombaltimoreoriole-and-a-male-red-breasted-grosbeak.jpg?itok=mGKiNpgF"></li>
      <li><img class="logo" alt="Temporary Logo" src="https://nas-national-prod.s3.amazonaws.com/styles/hero_image/s3/web_groombaltimoreoriole-and-a-male-red-breasted-grosbeak.jpg?itok=mGKiNpgF"></li>
      <li><img class="logo" alt="Temporary Logo" src="https://nas-national-prod.s3.amazonaws.com/styles/hero_image/s3/web_groombaltimoreoriole-and-a-male-red-breasted-grosbeak.jpg?itok=mGKiNpgF"></li>
      <li><img class="logo" alt="Temporary Logo" src="https://nas-national-prod.s3.amazonaws.com/styles/hero_image/s3/web_groombaltimoreoriole-and-a-male-red-breasted-grosbeak.jpg?itok=mGKiNpgF"></li>
      <li><img class="logo" alt="Temporary Logo" src="https://nas-national-prod.s3.amazonaws.com/styles/hero_image/s3/web_groombaltimoreoriole-and-a-male-red-breasted-grosbeak.jpg?itok=mGKiNpgF"></li>
      <li><img class="logo" alt="Temporary Logo" src="https://nas-national-prod.s3.amazonaws.com/styles/hero_image/s3/web_groombaltimoreoriole-and-a-male-red-breasted-grosbeak.jpg?itok=mGKiNpgF"></li>
      <li><img class="logo" alt="Temporary Logo" src="https://nas-national-prod.s3.amazonaws.com/styles/hero_image/s3/web_groombaltimoreoriole-and-a-male-red-breasted-grosbeak.jpg?itok=mGKiNpgF"></li>
      <li><img class="logo" alt="Temporary Logo" src="https://nas-national-prod.s3.amazonaws.com/styles/hero_image/s3/web_groombaltimoreoriole-and-a-male-red-breasted-grosbeak.jpg?itok=mGKiNpgF"></li>
    </ul>
    <button v-on:click="test">test</button>
  </div>
</template>

<script>

export default {
  name: 'SoundsOfImpact',
  data () {
    return {
      bird1: '',
      msg: ''
    }
  },
created: function () {
    //this.function()
    },
  methods: {
     test: function () {
     this.bird1 = 'https://www.scitecheuropa.eu/wp-content/uploads/2019/09/Colour-bird-e1568033112774.jpg';
     this.msg = 'sounds of human impact'
     }
  },
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.logo {
height: 200px; 
}
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
