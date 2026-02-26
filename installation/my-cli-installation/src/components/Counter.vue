<template>
  <div>
    <p>Count: {{ count }}</p>
    <p>Double: {{ doubleCount }}</p>
    <button @click="increment">Increment</button>
  </div>
</template>

<script>
export default {
    name: "CounterButton",
  data() {
    return { count: 0 }
  },
  methods: {
    increment() { this.count += 1 }
  },
  computed: {
    doubleCount() {
      return this.count * 2
    }
  }
}
</script>