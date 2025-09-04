//Html
<template>
    <div class="counter-wrapper">
        <button @click="increaseCount">Increase</button>

        <!-- attribute binding -->
        <h2 v-bind:class="counterStyle"> {{ count }} </h2>

        <!-- shortform attribute binding -->
        <!-- <h2 :class="counterStyle"> {{ count }} </h2> -->

        <button @click="decreaseCount">Decrease</button>
        
    </div>
    <h1>All Inbuild Directives</h1>
    
    <!-- v-html -->
    <div>
        <div v-html="rawHtml"></div> 
    </div>

    <!-- v-show (default is visible) -->
    <div>
        <p v-show="isVisible">Now you see me!</p>
        <button @click="isVisible = !isVisible">Toggle</button>
    </div>
    

    <!-- [v-if, v-else-if, v-else] -->
    <div>
        <p v-if="score > 90">Grade: A</p>
        <p v-else-if="score > 75">Grade: B</p>
        <p v-else>Grade: C</p>
    </div>


    <!-- v-for -->
    <div>
        <ul>
            <li v-for="(item, index) in items" :key="index">{{ index + 1 }}. {{ item }}</li>
        </ul>
    </div>

    <!-- v-on -->
     <div>
        <button v-on:click="sayHello">Click Me</button>
        <button @click="sayHello">Click Me(shorthand)</button>
     </div>

     <!-- v-bind [dynamically bind the html attributes]-->
     <div>
        <img v-bind:src="imageUrl" :alt="altText" width="150"></img>
     </div>


     <!-- v-model -->
      <div>
        <input v-model="username" placeholder="Enter your name"></input>
        <p>Hello, {{ username }}</p>
      </div>

</template>
 

//CSS
<style scoped>
    * {
        margin: 20px;
        padding: 20px;
        box-sizing: border-box;
    }

    .counter-wrapper {
        display: flex;
        justify-content: center;
    }

    .success {
        color: green;
    }
    
    .normal {
        color: royalblue;
    }

    .danger {
        color: red;
    }
</style>


// JavaScript
<script>
import { ref } from 'vue';
export default {
    data() {
        return {
            counterStyle: "normal",
            count: 0, // also called state variables,
            rawHtml: "<strong>This is bold text </strong>",
            isVisible : ref(true),
            score: 82,
            items: ["Vue", "React", "Angular"],
            imageUrl: "https://vuejs.org/images/logo.png",
            altText: "Vue Logo",
            username: ref("")
        }
    },
    methods: {
        increaseCount(){
            this.count++;
            if(this.count > 10){
                this.counterStyle = "success"
            }
        },
        decreaseCount() {
            this.count--;
            if(this.count < 0){
                this.counterStyle = "danger"
            }
        },
        sayHello(){
            alert("Hello from Vue!")
        }
    }
}
</script>