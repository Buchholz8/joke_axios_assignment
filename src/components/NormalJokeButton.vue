<template>
  <div>
    <button @click="this.$emit(`norm_handle`, this.base_joke)">Normal Joke</button>
  </div>
</template>

<script>
export default {
  methods: {
    norm_handle: function(details) {
      this.base_joke = details
    }
  },
  data( ) {
    return{
      base_joke: undefined,
    }
  },
  mounted(){
    this.$root.$on(`get_joke` , this.norm_handle)
  }
}
</script>

<style scoped>
</style>