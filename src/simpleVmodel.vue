<script setup>
import { ref } from 'vue'

const message = ref('')
</script>

<template>
<h5>define ref and v-model</h5>
  <p>Message is: {{ message }}</p>
<textarea v-model="message"></textarea>

</template>