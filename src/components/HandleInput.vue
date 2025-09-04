<template>
    <input @input="(e)=>handleInput(e.target.value)"/>
    <div>{{ name }}</div>
</template>


<script>
    export default{
        data(){
            return{
                name: ""
            }
        },
        methods:{
            handleInput(value){
                this.name = value
            }
        }
    }
</script>



<style>

</style>