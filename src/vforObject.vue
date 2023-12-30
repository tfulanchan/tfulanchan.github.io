<script setup>
import { reactive } from 'vue'

const myObject = reactive({
  title: 'How to do lists in Vue',
  author: 'Jane Doe',
  publishedAt: '2016-04-10'
})
</script>

<template>
<a href="https://vuejs.org/guide/essentials/list#v-for-with-an-object">source</a>
	<ul>
    <li v-for="(value, key, index) in myObject">
		  {{ index }}. {{ key }}: {{ value }}
		</li>
  </ul>
</template>