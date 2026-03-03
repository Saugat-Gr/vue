<template>
  <div>
    <h1>Parent Component</h1>
    <ChildComponent>
      <p>This is content passed from the parent via slot!</p>
    </ChildComponent>
  </div>
</template>

<script setup>
import ChildComponent from './ChildComponent.vue';
</script>