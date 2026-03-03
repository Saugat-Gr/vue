<template>
  <div id="app">
    <h1>Vue Feature Demo</h1>

    <section>
      <h2>Slots Demo</h2>
      <ChildComponent>
        <p>This is passed from App.vue using a slot!</p>
      </ChildComponent>
    </section>

    <section>
      <h2>Dynamic Components Demo</h2>
      <button @click="current = 'ComponentA'">Show Component A</button>
      <button @click="current = 'ComponentB'">Show Component B</button>
      <component :is="current"></component>
    </section>

    <section>
      <h2>Lifecycle Hooks Demo</h2>
      <LifecycleDemo v-if="showLifecycle" />
      <button @click="toggleLifecycle">Toggle Lifecycle Component</button>
    </section>
  </div>
</template>

<script setup>
import { ref } from 'vue';


import ChildComponent from './components/ChildComponent.vue';
import ComponentA from './components/ComponentA.vue';
import ComponentB from './components/ComponentB.vue';
import LifecycleDemo from './components/LifecycleDemo.vue';

const current = ref('ComponentA');

const showLifecycle = ref(true);
const toggleLifecycle = () => showLifecycle.value = !showLifecycle.value;
</script>

<style>
#app { font-family: Avenir, Helvetica, Arial, sans-serif; padding: 20px; }
section { margin-bottom: 30px; padding: 10px; border: 1px solid #ccc; }
button { margin-right: 10px; margin-top: 10px; }
</style>