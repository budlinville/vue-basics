<script setup>
  import { ref } from 'vue';

	import Child from './Child.vue';
  
  const text = ref('');
  const visible = ref(true)
</script>

<template>
	<div>
    <input v-model='text'/>
    <button @click="visible = !visible">
    	Toggle Child
    </button>
    <Child v-if="visible" :text="text" />
  </div>
</template>

<style>

  
</style>
