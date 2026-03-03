<!-- DynamicComponentDemo.vue -->
<template>
  <div>
    <h1>Dynamic Components Example</h1>
    <button @click="current = 'ComponentA'">Show Component A</button>
    <button @click="current = 'ComponentB'">Show Component B</button>

    <!-- Dynamic component rendering -->
    <component :is="current"></component>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import ComponentA from './ComponentA.vue';
import ComponentB from './ComponentB.vue';

const current = ref('ComponentA');
</script>