<template>
    <div>
        <button @click="this.$emit(`loud_joke`, this.loud_joke)"> Loud Joke</button>
    </div>
</template>

<script>
    export default {
        data( ) {
            return{
                loud_joke:`this is loud`
            }
        },
    }
</script>

<style scoped>

</style>