<script setup>
  import { reactive, ref, watchEffect, watch } from "vue";

  const counter = ref(0);
  const date = ref(new Date().toLocaleTimeString());
  function counterHandler(event) {
    console.log();
    counter.value++;
  }

  watch(
    {},
    () => {
      setInterval(() => {
        date.value = new Date().toLocaleTimeString();
      }, 1000);
    },
    { immediate: true }
  );
</script>

<template>
  <button @click="counterHandler">counter {{ counter }}</button>
  <h1>{{ date }}</h1>
</template>

<style scoped></style>
