<script setup>
	import { reactive, computed, ref } from 'vue';
  
  const bgColor = ref('white')
  const textColor = ref('black');
  
  const toggleBg = () => bgColor.value = bgColor.value == 'white'
  	? 'red' 
  	: 'white';
  const toggleText = () => textColor.value = textColor.value == 'black'
  	? 'blue'
  	: 'black';
  
</script>

<template>
  <div>
    <button v-on:click="toggleBg">Red</button>
    <button @click="toggleText">Blue</button>
    <div
      class="greenBorder"
      :style="{ 'background-color': bgColor, color: textColor }">
      <h1>Hello!</h1>
    </div>
  </div>
</template>

<style>
  .redBg {
    background-color: red;
  }
  
  .blueText {
    color: blue;
  }
  
  .greenBorder {
    border: 5px solid green;
  }
</style>
