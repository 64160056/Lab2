<script setup lang="vs">
import { ref } from 'vue'
</script>

<template>
  <p>
    <span title="message">
      Hover your mouse over me for a few seconds to see my dynamically bound
      title!
    </span>
  </p>
  <p class="red">
    <span>This should be red... but click me to toggle it.</span>
  </p>
  <p style="color: green">
    <span>This should be red... but click me to toggle it.</span>
  </p>
</template>

<style scoped></style>
