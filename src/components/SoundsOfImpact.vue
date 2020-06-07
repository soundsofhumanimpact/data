<template>
  <div>
    <h1>{{ msg }}</h1>
    <ul id="birds" >
      <li><img class="card" :alt="birdName1" :src="birdImage1">{{birdName1}}</li>
      <li><img class="card" :alt="birdName2" :src="birdImage2">{{birdName2}}</li>
      <li><img class="card" :alt="birdName3" :src="birdImage3">{{birdName3}}</li>
      <li><img class="card" :alt="birdName4" :src="birdImage4">{{birdName4}}</li>
    </ul>
    <button v-on:click="test">test</button>
    <button v-on:click="getData">prime</button>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'SoundsOfImpact',
  data () {
    return {
      msg: '', 
      birdName1: '', 
      birdImage1: '', 
      birdSound1: ''
    }
  },
created: function () {
    //this.function()
    },
  methods: {
     test: function () {
     this.bird1 = 'https://www.scitecheuropa.eu/wp-content/uploads/2019/09/Colour-bird-e1568033112774.jpg';
     this.msg = 'Sounds of Human Impact'
     },
     getData: function () {
       axios.get("https://raw.githubusercontent.com/soundsofhumanimpact/app/master/birdData.JSON")
       .then(function (response) {
       console.log(response)
       
          this.birdName1 = response.raptors[1].common
          this.birdImage1 = response.raptors[1].image
          this.birdSound1 = response.raptors[1].sound1
          var audio1 = new Audio(this.birdSound1);
          audio1.play();
          
          this.birdName2 = response.raptors[2].common
          this.birdImage2 = response.raptors[2].image
          this.birdSound2 = response.raptors[2].sound1
          var audio2 = new Audio(this.birdSound2);
          audio2.play();
          
          this.birdName3 = response.finches[1].common
          this.birdImage3 = response.finches[1].image
          this.birdSound3 = response.finches[1].sound1
          var audio3 = new Audio(this.birdSound3);
          audio3.play();
          
          this.birdName4 = response.finches[2].common
          this.birdImage4 = response.finches[2].image
          this.birdSound4 = response.finches[2].sound1
          var audio4 = new Audio(this.birdSound4);
          audio4.play();
          
       })
       .catch((error) => {
       console.log(error)
       })
    }
  },
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
height: 200px; 
color: black; 
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
