<script setup>
	import { ref } from 'vue';
	
	const count = ref(1)
  
  // Can throw raw HTML in here... cannot throw Vue code in here
	const arbitraryHtmlStr = "<h3>{{count}}</h3><button @click='count++'>+1</button>"
</script>

<template>
  <h3>{{count}}</h3>
	<span v-html="arbitraryHtmlStr"/>
  <button @click='count++'>+1</button>
</template>