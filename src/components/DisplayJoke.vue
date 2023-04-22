<template>
    <div>
        <p> Get A Joke </p>
        <p> {{OG_Joke}} </p>
        <button @click="base_joke"> Display Joke </button>
        
    </div>
</template>

<script>
    export default { 
        //i made a data with something called OG_Joke to be the thing being styled
        data() {
            return {
                OG_Joke: undefined,
            }
        },
        //i have a methods list to change the value of OG_Joke depending on the function sent from app.vue
        methods: {
            base_joke(new_joke){
                this.OG_Joke = new_joke
            },
            new_joke(joke){
                this.OG_Joke = joke
            },
            snakey_joke(loud){
                this.OG_Joke = loud
            },
            loud_joke(snake){
                this.OG_Joke = snake
            }
        },
        //i have a mounted area to grab the functions from app.vue
        mounted( ){
            this.$on(`base_joke` , this.base_joke)
            this.$on(`normal_joke` , this.new_joke)
            this.$on(`base_joke` , this.base)
            this.$on(`loud_joke` , this.loud)
        }
    }
</script>

<style scoped>

</style>