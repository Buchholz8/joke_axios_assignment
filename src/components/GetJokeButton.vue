<template>
  <div>
    <button @click="this.$emit(`get_joke`, base_joke)">Get Joke</button>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data: {
    return: {
      base_joke: undefined,
    },
  },
  mounted() {
    axios
      .request({
        url: `https://ron-swanson-quotes.herokuapp.com/v2/quotes`,
      })
      .then((response) => {
        this.base_joke = response[`data`]
      })
      .catch((error) => {
        error;
      });
  },
};
</script>

<style scoped>
</style>