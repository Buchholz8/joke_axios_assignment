<template>
    <div>
        <p> Get A Joke </p>
        <p> {{OG_Joke}} </p>
        <button @click="base_joke"> Display Joke </button>
        
    </div>
</template>

<script>
    export default { 
        data() {
            return {
                OG_Joke: undefined,
            }
        },
        methods: {
            base_joke(new_joke){
                this.OG_Joke = new_joke
            },
            new_joke(joke){
                this.OG_Joke = joke
            },
            snakey_joke(loud){
                this.OG_Joke = loud.split(` `).join(`_`)
            },
            loud_joke(snake){
                this.OG_Joke = [snake].toUpperCase
            }
        },
        mounted( ){
            this.$on(`base_joke` , this.base_joke)
            this.$root.$on(`normal_joke` , this.new_joke)
            this.$root.$on(`base_joke` , this.base)
            this.$root.$on(`loud_joke` , this.loud)
        }
    }
</script>

<style scoped>

</style>