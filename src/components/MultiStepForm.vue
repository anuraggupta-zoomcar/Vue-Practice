<template>
    <form action="">
        <div v-if="step === 1">
            <label>Name</label>
            <input type="text" />
        </div>
        <div v-else-if="step === 2">
            <label>Email</label>
            <input type="text"/>
        </div>
        <div v-else>
            <label>Password</label>
            <input type="password"/>
        </div>
        <button type="button" @click="handleNextButton">{{ step <= 2 ? "Next" : "Submit" }}</button>
    </form>

</template>


<script>
    export default {
        data(){
            return {
                step: 1
            }
        },
    methods:{
        handleNextButton(){
            if(this.step < 3){
                this.step = this.step + 1
            }
        }
    }}
</script>


<style>
    
</style>