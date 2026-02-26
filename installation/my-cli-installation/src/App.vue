<template>

  <div id="app">
    <h1>Creating of User Cards:</h1>
    <UserCard userName="Saugat Gurung" age="21"></UserCard>
    <Counter></Counter>
  </div>

</template>


<script>

import UserCard from './components/UserCard.vue';
import Counter from './components/Counter.vue';

export default{
  name: "App",
  components:{
     UserCard, Counter
  }
}

</script>