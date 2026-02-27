<template>
    <div class="test">
    <h1>Hello {{ name }}!</h1>
    <input type="text" v-model="name" placeholder="Enter your name">
    <input type="number" v-model="age" placeholder="Enter your age">
    <button @click="verifyUser">Verify Age</button>
    <p>{{ displayProfile }}</p>
    <p v-if="aboveAge">You are above 18 years old.</p>
    <p v-else>You are below 18 years old.</p>
    </div>
</template>


<script>
export default {
    data() {
        return {
            name: '',
            age: 0,
            aboveAge:false
        }
    },
    computed: {
        displayProfile() {
         return `My name is ${this.name} and i am ${this.age}`;
        }
    },
    methods: {
         verifyUser() {
         if(this.age < 18){
         this.aboveAge = false
        } else {
        this.aboveAge = true    
           }
        },   
    },

    watch: {
        name(newValue) {
            console.log(`Name changed to: ${newValue}`);
        },
        age(newValue) {
            this.verifyUser();
             console.log(`Age changed to: ${newValue}`);
        }
    },
    
    mounted() {
        console.log('Application mounted');
    },
}
</script>


<style scoped>

p{
    color:black;    
}

 h1{
   color: red;
 }
 
</style>