<template>
  <div id="app">
    <h1> {{ person }}</h1>
  </div>
</template>

<script>
import axios from 'axios'
import URL from './services/url.js'
import { ServerResponse } from 'http';

export default {
  name: 'app',
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
</style>
