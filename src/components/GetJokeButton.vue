<template>
  <div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      base_joke: undefined,
    }
  },
  mounted() {
    axios
      .request({
        url: `https://ron-swanson-quotes.herokuapp.com/v2/quotes`,
      })
      .then((response) => {
        this.$emit(`new_joke` , response[`data`][0])
      })
      .catch((error) => {
        error;
      });
  },
};
</script>

<style scoped>
</style>