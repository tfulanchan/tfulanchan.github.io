<script setup>
import { reactive, ref, computed } from 'vue'

const count = ref(0)
const state = reactive({
  count
})
const books = reactive([ref('Vue 3 Guide')])
const map = reactive(new Map([['count', ref(0)]]))
const object = { id: ref(1) }
const { id } = object

</script>

<template>
<h5>reactive</h5>
<a href="https://vuejs.org/api/reactivity-core.html#reactive">source</a>
<p> {{ count }} </p>
<p> {{ state.count }} </p>
<p> {{ count.valueOf }} </p>
<p> {{books[0].value}} </p>
<p> {{map.get('count').value}} </p>
<p> {{ object.id }} </p>


</template>