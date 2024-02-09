<script setup>
import { ref, onUnmounted } from 'vue';
const crossed = ref(false);

const int = setInterval(() => {
  crossed.value = !crossed.value;
}, 500);

onUnmounted(() => {
  clearInterval(int);
});
</script>

<template>
  <h1 style="font-size: 10rem">
    {{ crossed ? '🤞' : '✌️' }}
  </h1>
</template>
