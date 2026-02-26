<template>

  <div class="user-card">
         <h2>{{ userName }} - Age {{ age }}</h2>
         <button @click="greet">Say Hi</button>
  </div>

</template>


<script>

  export default{
       name: "UserCard",
       props: ['userName', 'age'],
       data(){
          return {
             isActive: true
          }
       },
       methods:{
          toggleActive(){
             this.isActive = !this.isActive;
          },

          greet(){
              console.log("Hello WOrld");
          }
       },
       mounted(){
         console.log('UserCard mounted');
       }
  }

</script>


<style scoped>
.user-card {
  border: 1px solid #ccc;
  padding: 10px;
  border-radius: 5px;
  background-color: #f8f8f8;
}
</style>