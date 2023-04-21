<template>
  <div id="app">
<normal-joke-button></normal-joke-button>
  </div>
</template>

<script>
import NormalJokeButton from '@/components/NormalJokeButton.vue'

export default {
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
