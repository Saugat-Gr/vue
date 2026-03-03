
<template>
  <div class="child-box">
    <h2>Child Component</h2>
    <slot>
      <p>No content provided from parent.</p>
    </slot>
  </div>
</template>

<script setup>
</script>

<style scoped>
.child-box { border: 1px solid #333; padding: 10px; }
</style>