<template>
    <input type="text" v-model="username"> <br>
    <input type="text"> <br>
    <input type="submit" @click="submit()">
    <div v-if="!username.length">
        You must provide data!!
    </div>

</template>

<script>
export default{
    data () {
        return {
            username: ""
        }
    },
    methods: {
        submit () {
            if(this.username == "suka") {
                alert("Fuck off")
            }
        }
    }
}
</script>

<style>
</style>

