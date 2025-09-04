<!-- modifiers:
1. lazy
2. number
3. trim -->



<!-- HTML -->
<template>

    <p>{{ form }}</p>

    <br/> 
    <br/> 
    <br/> 
 
    <p>Message is: {{ message }}</p>
    <input v-model="form.message" placeholder="edit me"></input>

    <br />
    <br />
    <br />

    <p>Message is: {{ textArea }}</p>
    <textarea v-model="form.textArea" placeholder="text area"></textarea>

    <br />
    <br />
    <br />

    <label>Terms & Conditions</label>
    <input type="checkbox" v-model="form.termAndConditions"></input>

    <br />
    <br />
    <br />

    <!-- checkbox -->
    <label>Admins</label>
    <label>
        Anurag <input type="checkbox" v-model="form.admins" value="Anurag"></input>
    </label>
    <label>
        Aditya <input type="checkbox" v-model="form.admins" value="Aditya"></input>
    </label>

    <br />
    <br />
    <br />

    <!-- Radio Buttons -->
    <label>Gender</label>
    <label>
        Male <input type="radio" v-model="form.gender" value="Male"></input>
        Female <input type="radio" v-model="form.gender" value="Female"></input>
    </label>

    <br/>
    <br/>
    <br/>

    <!-- Drop Down Tags -->
    <label>Select Laptop:</label>
    <select v-model="form.laptop">
        <option disabled value="">Select any one</option>
        <option value="hp">HP</option>
        <option value="asus">ASUS</option>
        <option value="dell">DELL</option>
        <option value="lenovo">Lenovo</option>
    </select>


    <br />
    <br />
    <br />

    <!-- Drop Down using API -->
    <label>Select Role:</label>
    <select v-model="form.dynamicRole">
        <option disabled value="">Select any one</option>
        <option v-for="role in computedSelectTagData" :value="role.value" >{{ role.text }}</option>
    </select>
   
</template>



<!-- JS -->
<script>
    export default{
        data(){
            return{
                form:{
                    message: "",
                    textArea: "",
                    termAndConditions: false,
                    admins: [],
                    gender: "",
                    laptop: "",
                    dynamicRole: ""
                }
                
            }
        },
        methods: {
            dynamicSelectDropdown(){
                return [
                    { text: "Full Stack", value: "fullstack" },
                    { text: "Front End", value: "frontend" },
                    { text: "Back End", value: "backend" }
                ]
            }
        },
        mounted(){
            this.dynamicSelectDropdown()
        },
        computed: {
            computedSelectTagData(){
                return this.dynamicSelectDropdown()
            }
        }
    }
</script>



<!-- CSS -->
<style>

</style>