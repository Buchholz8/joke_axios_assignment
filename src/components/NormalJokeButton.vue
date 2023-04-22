<template>
  <div>
    <button @click="(response) => {this.norm_joke = response.data}">Joke</button>
    <p>{{ norm_jokes }}</p>
  </div>
</template>

<script>
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
        url: `https://ron-swanson-quotes.herokuapp.com/v2/quotes`,
      })
      .then((response) => {
        this.norm_jokes = response.data;
      })
      .catch((error) => {
        error;
      });
  },
};
</script>

<style scoped>
</style>