<script setup lang="ts">
import { ref } from "vue";
const text = ref("Edit Me");
const checked = ref(true);
const checkedNames = ref(["Jack"]);
</script>

<template>
  <h2>Text Input</h2>
  <input v-model="text" /> {{ text }}

  <h2>Checkbox</h2>
  <input type="checkbox" v-model="checked" id="checkbox" />
  <label for="checkbox">checked: {{ checked }}</label>

  <h2>Multi Checkbox</h2>
  <input type="checkbox" id="jack" value="Jack" v-model="checkedNames" />
  <label for="jack">Jack </label>
  <input type="checkbox" id="john" value="John" v-model="checkedNames" />
  <label for="john">John </label>
  <input type="checkbox" id="mike" value="Mike" v-model="checkedNames" />
  <label for="mike">Mike</label>
  <p>Checked names:</p>
  <pre>{{ checkedNames }}</pre>
</template>
