<template>
    <div>
        <button @click="this.$emit(`loud_button`, this.Loudly)"> Loud Joke</button>
    </div>
</template>

<script>
    export default {
methods :  {
   Loudly: function(details){
    details.split(` `).join(`_`)
   }
}
    }
</script>

<style scoped>

</style>