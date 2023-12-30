<script setup>
import { ref, onMounted } from 'vue'
import BlogPost from './Blogpost.vue'
const list = ref([1, 2, 3])
const itemRefs = ref([])
const posts = ref([
  { id: 1, title: 'My journey with Vue' },
  { id: 2, title: 'Blogging with Vue' },
  { id: 3, title: 'Why Vue is so fun' }
])
const postFontSize = ref(1)
</script>

<template> 
	<div :style="{ fontSize: postFontSize + 'em' }">
    <BlogPost
      v-for="post in posts"
      :key="post.id"
      :title="post.title"
      @enlarge-text="postFontSize += 0.1"
      @min-text="postFontSize -= 0.1"
    ></BlogPost>
  </div>
    <ul>
    <li v-for="item in list" ref="itemRefs">
      {{ item }}
    </li>
  </ul>
</template>