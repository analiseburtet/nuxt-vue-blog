<template>
    <div class="container">
        <input type="text" v-model="userId">
        <button @click="onLoadUser">Load User</button>
        <nuxt-child/>
    </div>
</template>

<script>
    export default {
        data(){
            return {
                userId: ""
            }
        },
        methods: {
            onLoadUser(){
                this.$router.push("/users/" + this.userId)
            }
        }
    }
</script>