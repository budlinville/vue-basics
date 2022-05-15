<script setup>
  import { onMounted, onUpdated, onUnmounted } from 'vue';
  
	defineProps({
    text: String,
  });
  
  onMounted(() => {
    console.log('Mounted')
  });
  
  onUnmounted(() => {
    console.log('Unmounted')
  });
  
  onUpdated(() => {
    console.log('Updated')
  });
</script>

<template>
	<div>
        <h3>{{text}}</h3>
    </div>
</template>

<style>

</style>