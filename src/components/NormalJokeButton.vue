<template>
  <div>
    <button @click="normal_joke">Joke</button>
    <p>{{ jokes }}</p>
  </div>
</template>

<script>
export default {
    data() {
        return{
            jokes: `Jokes`,
         }
    },
  methods: {
    normal_joke: function (details) {
      this.jokes = details;
    },
  },
  mounted() {
    this.$root.$on(`handle_norm_joke`, this.normal_joke);
  },
};
</script>

<style scoped>
</style>