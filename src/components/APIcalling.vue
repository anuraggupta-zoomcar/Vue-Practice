<template>
    <br />
    <br />
    <br />

    <input placeholder="Enter Question" v-model="question" :disabled="loading"></input>
    <p>{{ answer }}</p>
</template>

<script>
    export default{
        data(){
            return{
                loading: false,
                answer: "",
                question: ""
            }
        },
        watch: {
            question(newQuestion){
                if(newQuestion.includes('?')){
                    this.getAnswer()
                }
            }
        },
        methods: {
            async getAnswer(){
                this.loading = true
                this.answer = "Thinking..."
                try {
                    const res = await fetch("https://yesno.wtf/api");
                    this.answer = (await res.json()).answer
                }catch(error){
                    this.answer = "Error! Could not reach the API," + error
                }finally{
                    this.loading = false
                }
            }
        }
    }
</script>

<style>

</style>


