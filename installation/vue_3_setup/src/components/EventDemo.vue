<template>
  <div>
    <h2>{{ count }}</h2>
    <button @click="increment">Increase</button>
    <button @click="decrement">Decrease</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const count = ref(0)

function increment() {
  count.value++
}

function decrement() {
  count.value--
}
</script>