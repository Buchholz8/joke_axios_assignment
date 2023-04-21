<template>
  <div>
    <button>Normal Joke</button>
    <div v-for="(joke, i) in jokes" :key="i">
      <p>{{ joke }}</p>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      jokes: undefined,
    };
  },
  mounted() {
    axios.request({
        url: `https://ron-swanson-quotes.herokuapp.com/v2/quotes`,
      })
      .then((response) => {
        this.joke = response[`data`][`data`];
      })
      .catch((error) => {
        error;
      });
  },
};
</script>

<style scoped>
</style>