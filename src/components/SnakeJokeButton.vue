<template>
    <div>
        <button @click="this.$emit(`snakey_joke`, this.snake_joke)"> Snake Joke </button>
    </div>
</template>

<script>
    export default {
        data( ) {
            return{
                snake_joke:`this is very much a snake`
            }
        },
    }
</script>

<style scoped>

</style>