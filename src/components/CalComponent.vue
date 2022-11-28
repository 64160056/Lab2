<script lang="ts">
import { reactive, computed } from "vue";
export default {
  setup() {
    const state = reactive({
      num1: "0",
      num2: "0",
      result: 0,
    });
    const result = computed(function () {
      return parseInt(state.num1) + parseInt(state.num2);
    });
    function add() {
      state.result = parseInt(state.num1) + parseInt(state.num2);
    }
    return { state, add, result };
  },
};
</script>

<template>
  <div class="card">
    <div>
      <input
        v-model="state.num1"
        type="text"
        ref="num1"
        style="text-align: center; width: 80%"
      />
    </div>
    <div>+</div>
    <div>
      <input
        v-model="state.num2"
        type="text"
        ref="num1"
        style="text-align: center; width: 80%"
      />
    </div>
    <hr />
    <button @click="add" style="width: 80%">=</button>
    <div ref="result">
      {{ state.num1 }}+{{ state.num2 }} = {{ state.result }}
    </div>
  </div>
</template>

<style></style>
