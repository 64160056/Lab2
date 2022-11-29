<script setup lang="ts">
import { ref } from "vue";
const message = ref("Hello World");
</script>

<template>
  <h1>{{ message }}</h1>
  <button>Revere Message</button>
  <button v-on:click="message += '!'">Append "!"</button>
  <a href="">A link with e.preventDefault</a>
</template>

<style scoped>
button,
a {
  display: block;
  margin-bottom: 1em;
}
</style>
