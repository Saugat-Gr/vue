<template>
  <div>
    <h1>Check console for lifecycle hooks</h1>
  </div>
</template>

<script setup>
import { onMounted, onUpdated, onBeforeUnmount } from 'vue';

onMounted(() => {
  console.log('Component mounted!');
});

onUpdated(() => {
  console.log('Component updated!');
});

onBeforeUnmount(() => {
  console.log('Component will unmount!');
});
</script>