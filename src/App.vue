<template>
  <div id="app">
    <div class="container-left">
    <PFHero v-bind:person="person"></PFHero>
    <PFImformacion v-bind:person="person"></PFImformacion>
    </div>
    <div class="container-right">
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import URL from './services/url.js'

//Componenets
import PFHero from '../src/components/Hero.vue'
import PFImformacion from '../src/components/Informacion.vue'

export default {
  name: 'app',
  components: {
    PFHero,
    PFImformacion
  },
  data () {
    return { 
      person: [],
    }
  },
  mounted() {
    axios
      .get(URL)
      .then(response => (this.person = response))
      console.log(this.person)
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
}
h1,h2,h3,p {
  font-family: 'ABeeZee', sans-serif; 
}
p {
  font-size: 20px;
}
#app {
  display: flex;
  width: 100%;
  height: 100vh;
}
.container-left{
  background-color: #252f63;
  color: #fff;
  width: 50%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.container-right {
  background-color: #000000;
  width: 50%
}
</style>
