<template>
  <div id="app">
<normal-joke-button :post="norm_joke"></normal-joke-button>
  </div>
</template>

<script>
import NormalJokeButton from '@/components/NormalJokeButton.vue'

import axios from "axios";
export default {
      methods: {

    },
  data() {
    return {
      norm_jokes: undefined,
    };
  },
  mounted() {
    axios
      .request({
        url: `https://ron-swanson-quotes.herokuapp.com/v2/quotes`
      })
      .then((response) => {
        this.norm_joke = response[`data`]
        this.$emit(`handler_norm_joke` , response[`data`])
      })
      .catch((error) => {
        error;
      });
  },



  name: 'App',
  components: {
NormalJokeButton,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
