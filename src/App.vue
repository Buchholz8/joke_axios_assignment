<template>
  <div id="app">
    <display-joke></display-joke>
    <get-joke-button> </get-joke-button>
    <normal-joke-button ></normal-joke-button>
    <snake-joke-button></snake-joke-button>
    <loud-joke-button></loud-joke-button>
  </div>
</template>

<script>
import NormalJokeButton from '@/components/NormalJokeButton.vue';
import GetJokeButton from '@/components/GetJokeButton.vue';
import DisplayJoke from '@/components/DisplayJoke.vue';
import SnakeJokeButton from '@/components/SnakeJokeButton.vue';
import LoudJokeButton from '@/components/LoudJokeButton.vue';

export default {
  methods: {
    get_joke(base_joke) {
      this.$root.$emit(`base_joke` , base_joke)
    },
    return_joke(joke) {
      this.$root.$emit(`normal_joke` , joke)
    },
    make_loud(loud){
      this.$root.$emit(`loud_joke` , loud)
    },
    make_snakey(snake){
      this.$root.$emit(`snakey_jokes` , snake)
    }
  },


  name: 'App',
  components: {
NormalJokeButton,
GetJokeButton,
DisplayJoke,
SnakeJokeButton,
LoudJokeButton,
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
