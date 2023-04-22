<template>
    <div>
        <button @click="new_joke"> Display Joke </button>
        <p> {{OG_Joke}} </p>
    </div>
</template>

<script>
    export default { 
        data: {
            return: {
                OG_Joke: undefined,
            }
        },
        methods: {
            new_joke(details){
                this.OG_Joke = details
            }
        },
        mounted( ){
            this.$root.$on(`new_joke` , this.new_joke)
        }
    }
</script>

<style scoped>

</style>