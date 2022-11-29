<script setup lang="ts">
import { ref } from "vue";
const message = ref("Helllo World!");
const isRed = ref(true);
function toggleRed() {
  isRed.value = !isRed.value;
}
</script>

<template>
  <p>
    <span :title="message">
      Hover your mouse over me for a few seconds to see my dynamically bound
      title!
    </span>
  </p>
  <p :class="{ red: isRed }" @click="toggleRed">
    <span>This should be red... but click me to toggle it.</span>
  </p>
  <p style="color: green">
    <span>This should be red... but click me to toggle it.</span>
  </p>
</template>

<style scoped>
.red {
  color: red;
}
</style>
