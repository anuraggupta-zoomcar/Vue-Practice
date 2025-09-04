<!-- Dom Change / State Change / Async Operaion(API Call) -->


<template>
    <p>{{ count }}</p>
    <button @click="count++">Increase</button>
    <button @click="count--">Decrease</button>
</template>

<script>
    export default{
        data(){
            return{
                count: 0
            }
        },
        watch:{
            count(newValue, oldValue) {
                if(this.count % 2 == 0){
                    console.log("Divisible by 2", newValue, oldValue)
                }
            },
            "form.password"(newValue){
                const regularExpression = "some-regex"
                if(regularExpression.test(newValue)){
                    this.strenngth = "Strong"
                }else{
                    this.strength = "Weak"
                }
            }
        }
    }
</script>

<style></style>