<script setup>
  import { ref, reactive } from "vue";

  const text = ref("");
  const card = reactive({
    value1: "aa",
    value2: "bb",
    value3: "cc",
  });
</script>

<template>
  <input v-model="text" />
  <div v-for="(value, key, index) in card" :key="msg" v-if="text === '12'">
    <h1>{{ value }} : {{ key }} : {{ index }}</h1>
  </div>
</template>
