<template>
  <div>
    <h1>Parent Component</h1>
    <ChildComponent 
      :message="parentMessage" 
      @update-count="handleUpdate"
    />
    <p>Count in Parent: {{ count }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import ChildComponent from './components/ChildComponent.vue'

const parentMessage = 'Hello from Parent'
const count = ref(0)

function handleUpdate(amount) {
  count.value += amount
}
</script>