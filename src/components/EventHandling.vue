<template>
    <button @click="count++" >Click me</button>
    <h1>{{ count }}</h1>
</template>

<script>
    export default{
        data(){
            return{
                count: 0
            }
        },
        methods:{
            hanldeDblClick(){
                console.log("Double Clicked Event Happened!")
            }
        }
    }
</script>

<style>

</style>