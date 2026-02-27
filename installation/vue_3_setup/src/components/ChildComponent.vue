<template>
  <div>
    <h2>Child Component</h2>
    <p>Message from Parent: {{ message }}</p>
    <button @click="sendToParent">Increase Count</button>
  </div>
</template>

<script setup>
import { defineProps, defineEmits } from 'vue'

const props = defineProps({
  message: String
})

const emit = defineEmits(['update-count'])

function sendToParent() {
  emit('update-count', 1)
}
</script>